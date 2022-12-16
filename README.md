# Coalescent_Lottery_Metacommunity_model
Function for coalescent and lottery simulation of metacommunity biodiveristy with spatial explicit landscape structure, 
different local community size, and different local species filters

Lines for parallel simulations are included 


#########################################################################################################
# This is the general function that run simulations of metacommunity diversity in explicit landscapes
 It is a general function with several options 
 
 **Meta.pool:** Vector of species abundance in the "matacommunity" it is an external vector not affected by local dynamics
 
 **m.pool:** migration from the species pool. Is the probability that a reclutant is samples from the "metacommunity" vector
 
**Js:** is the vector of total community size along all local communities (e.g. comunity size proportional to area)
 
**id.module:** vector with local communities membership to spatial modules (externally estimated from landscape structure)
 
**M.dist:** matrix with distances between local communities (could be Euclidian, topological or other)
 
**m.max:** maximum migration between communities. Is migration when distance=0. Typically m.max=1 
 
**D50:** is the distance at which migration is half m.max
 
**id.fixed:** are communities that are not involved in the simulation (e.g. river outlet or connection with other metacommunities not simulated)
 
**D50.fixed, m.max.fixed:** fixed communities may have different dispersal Kernel
 
**comm.fixed:** vector of species abundances in the fixed community (e.g. Meta.pool)
 
**Lottery=** c(TRUE,FALSE) If FALSE only coalescent simulation is performed. If TRUE coalescent filling is followed by a lottery dynamic
 
**it:** number of iterations in the Lottery simulation
 
**prop.dead.by.it:** fraciton of the local community replaced in each iteration
 
**id.obs:** Communities for which diversity (alpha, beta) should be returned
 
#########################################################################################################

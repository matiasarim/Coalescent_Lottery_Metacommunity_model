# Coalescent_Lottery_Metacommunity_model
Function for coalescent and lottery simulation of metacommunity biodiveristy with spatial explicit landscape structure, 
different local community size, and different local species filters

Lines for parallel simulations are included 

#########################################################################################################
## This  function run simulations of metacommunity diversity in explicit landscapes. The model can run only a Coescent assembly or be folloed by a lottery simulation. 
Several proceses scenarios can be evaluated:  
The landascape strucure is represented by a distance imput matrix. This matrix can be estiamted from Ecludian distances between communities or topological distances in a graph thar represent landscape strcuture (previous to run the present code).
An external species pool 
A region of the landscape thath can provides inmmigrants to the metacommunity but is not affected by the dynamic (e.g. river outlet)
The code requiere recognize regions (e.g. impacted or not impacted areas or environments). These regions are only used for estimatig beta diversity in the output and can be fantasy data.
Differant total abundances in local caommunities (e.g. because of habtiat size or productivity)
Dispersal Kernel are considered here as an exponential decay with distance that can be adapted by a decay parameter. The parameter d50 indicates the distance at which dispersal decay to half it maximum value.


### PARAMETERS 
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

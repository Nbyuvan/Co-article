# CONTROLHAZARDS
## Introduction:
HiGuys!Todayweseethehazardstopicdoyouknowabouthazardsandwhatarethe types of hazards we will learn like when will hazard occur or if occur control how to solve thehazards methods we will see the above topic in this presentation.
## Hazard:
Hazardaretheproblemwithintheinstructionpipeline.Whenproblemoccurinthe instruction we can not excute the next instruction the following the clock cycle.
### TYPES:
1.Data hazards 2.Structuralhazards
3.Controlhazards
Herewecanseethecontrolhazards.Andwhenwilloccurandweseethesolvingmethods for control hazards
ControlHazardDefinition:
Controlhazardsoccurswheninstructionlikebranchorjumpinstruction inthepipeline. Also Control called Branching hazards.
Ifthebranchinstructionsuccessfulwemoveontothetarget.Butthebranchinstruction will not successful we execute the remaining instruction.
SolvingMethods:

Thereareseveralmethodstosolvethecontrolhazards.Herewecanseethesome important methods to solve the control hazards.They are,
1.	Stall
2.	BranchDelaySlots
 
1.	Stall
InthismethodweneedtostopfetchtheinstructionuntilthebranchorJumpinstructioncomplete.

### ForExample:
PC:200 I1 SUB R3,R2,R1 PC:204 I2 JMP 240 PC:208I3ANDR4,R5,R6 PC:240I4ADD R7,R8,R9
Explanationoftheinstructions:
1.	First,R1andR2betweensubtractandthenvaluestoresin R3.
2.	NextJumpinstructioncomesowemoveinto240memoryaddressinstructions.
3.	ThenaddtheR8 andR9storesthevalue inR7.
4.	NowwemoveontoMemoryaddress208.


![table](https://github.com/Nbyuvan/Co-article/assets/167392738/75f62c7f-38fc-411e-b803-4f537dcf211b)

 
WeuseStallmethodweneedtidelayJumpinstructionorBranchinstruction.SoAfter, Jump or Branch instructon will be done they fetch the correct instruction.
Here we see the above example, in the example first instruction do not have Jump instruction or Branch instruction.So the next instruction will be fetch when the first instruction will decode simultaneously. In the Second instruction we can see the Jump instructionthatisJMP240instructionuntilcompletetheotherinstructiondonotfetchthe instruction.
2.	BranchDelaySlots

Thebranch delay slothelp to keep the pipelineinstructions and theyimproving the performanceoftheprocessor. Byallowaninstructiontobeexecutedimmediatelyfollowing a branch instruction, regardless of whether the branch is taken or not, the processor can continue processing instructions without waiting for the branch condition to be resolved.
This is particularly helpful for in pipelined processors, where multiple instructions are executedsimultaneouslyinthepipeline.TheBranchdelayslotwithusefultheprocessor can minimize pipeline stallsstages and maintain performance.
Hereweseetheexamples:- a)


becomes

 
Youseethethisinstructionwritessomethingintor1andthisbranchisreadingr2thereno really data dependence between these two instructions if you reorder these two instructions you still end up with the program that has exactly the same result.
If instructiondonothave datadependencytheinstructionwillmovetothedelayslot.Ifin the instruction data dependency occur the instruction will not move to the delay slot.
In thisexample , add$r1,$r2,$r3
If$r2=0then Delay slot
Followingthisconditionwewillseethedelayslotwhatevertheinstructionexecuted regardless of the outcome of the condition.
If the condition is met $r2 equals 0, then the instruction in the delay slot will be executed alongwiththebranch instruction.Inthiscase,theadd instructionwillbeexecuted,adding the values in $r2 and $r3 and storing the result in $r1.
Iftheconditionisnotmet $r2isnotequalto0,theadd instructionwillstillbeexecuted,as the delay slot instruction is not dependent on the branch outcome.
Sowereordertheinstructionbecomes,

If $r2 = 0 then add$r1,$r2,$r3
intheinstructionwillexecutewedecreasetheinstructionlines.

 
WeuseStallmethodweneedtidelayJumpinstructionorBranchinstruction.SoAfter, Jump or Branch instructon will be done they fetch the correct instruction.
Here we see the above example, in the example first instruction do not have Jump instruction or Branch instruction.So the next instruction will be fetch when the first instruction will decode simultaneously. In the Second instruction we can see the Jump instructionthatisJMP240instructionuntilcompletetheotherinstructiondonotfetchthe instruction.
2.	BranchDelaySlots

Thebranch delay slothelp to keep the pipelineinstructions and theyimproving the performanceoftheprocessor. Byallowaninstructiontobeexecutedimmediatelyfollowing a branch instruction, regardless of whether the branch is taken or not, the processor can continue processing instructions without waiting for the branch condition to be resolved.
This is particularly helpful for in pipelined processors, where multiple instructions are executedsimultaneouslyinthepipeline.TheBranchdelayslotwithusefultheprocessor can minimize pipeline stallsstages and maintain performance.
Hereweseetheexamples:- a)


becomes

 
Youseethethisinstructionwritessomethingintor1andthisbranchisreadingr2thereno really data dependence between these two instructions if you reorder these two instructions you still end up with the program that has exactly the same result.
If instructiondonothave datadependencytheinstructionwillmovetothedelayslot.Ifin the instruction data dependency occur the instruction will not move to the delay slot.
In thisexample , add$r1,$r2,$r3
If$r2=0then Delay slot
Followingthisconditionwewillseethedelayslotwhatevertheinstructionexecuted regardless of the outcome of the condition.
If the condition is met $r2 equals 0, then the instruction in the delay slot will be executed alongwiththebranch instruction.Inthiscase,theadd instructionwillbeexecuted,adding the values in $r2 and $r3 and storing the result in $r1.
Iftheconditionisnotmet $r2isnotequalto0,theadd instructionwillstillbeexecuted,as the delay slot instruction is not dependent on the branch outcome.
Sowereordertheinstructionbecomes,
![diagram](https://github.com/Nbyuvan/Co-article/assets/167392738/3f9ec05b-bd95-40b9-bbe0-8c71a9488cf5)


If $r2 = 0 then add$r1,$r2,$r3
intheinstructionwillexecutewedecreasetheinstructionlines.

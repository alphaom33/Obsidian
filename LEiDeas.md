States:
	Game:
		Disabled
		Auto
		Teleop
		Endgame
	Everything In
	Started
	Elevator:
		Low
		L2
		L3
		L4
		Barge
	CoralArm:
		ninetyish
		onethirtyfive
		in
	AlgeeArm:
		up
		high
		low
	Algee wheel spinning (speed?)
	PositionStates:
		near reef
		near hp station
		near porcessor
		near barge
		Parking?
	Centering:
		Reef spot?
		Coral
		Algee
		Porcessor
	Limelight:
		Seeing things
		Num things?
		What things?
	Robot speed or accel
	add up all pid errors


```mermaid
graph TD

endgame{endgame}

conglaturations --time--> movement
style conglaturations fill:#f9f,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5
sad --time--> movement
style sad fill:#ddf,stroke:#44a,strok-width:2px

subgraph scoring
	coralCentering --centered--> flash --time--> coralRising --setpoint--> anticipation
end
anticipation --getToScoreWithArm--> conglaturations
scoring --endEarly--> sad

subgraph beginning
	start <-.rnd.-> rainbow & otherspares --enabled--> goingOut -- out--> autoMovement
	autoMovement --elevator--> rising --setpoint--> autoAnticipation --finish--> autoConglaturations --time--> autoMovement
	autoMovement --byHpStation--> autoHping --leave--> autoMovement
end
beginning --teleop--> movement

movement --scorewitharm--> coralCentering

movement --byReef--> reefing --leave--> movement
movement --byHpStation--> hping --leave--> movement
movement --byBarge--> endgame
endgame --true--> parking --leave--> movement
endgame --false--> barging --leave--> movement

subgraph bargeScoring
	bargeRising --algeeSpinning--> bargeAlgeeSpinning
end
bargeScoring --finish--> conglaturations
movement --bargeHeight--> bargeRising

subgraph porcessorScoring
	porcessorCentering --centered--> lowering --setpoint--> porcessorAlgeespinning
end
porcessorScoring --finish--> conglaturations
movement --byPorcessor--> porcessoring --leave--> movement  
movement --centerOnPorcessor--> porcessorCentering

movement --IntakeAlgeeCommand--> algeeRising
subgraph algeeIntaking
	algeeRising --setpoint--> algeespinning & algeeCentering 
end
algeeIntaking --intaked--> conglaturations

movement --endgame--> b((double deltaTime))
```

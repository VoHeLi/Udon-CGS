# Udon-CGS
Udon Climbing/Gliding/Swimming System (VR Only)


(Using Cancerspace for underwater effects)

#How to use Udon CGS System :

- Install VRChat SDK (with Udonsharp) if it is not already done, and setup layers by testing your world (Verify every object Networking is in manual except climbingstations)
- Setup layers 23(Climbable surfaces), 24(Swimming volumes), and 25(Climbing Stations) (Edit -> Project Settings... -> Physics)
(Look at the image layers.png)
- Import CGS Package and drag and drop Udon CGS System in the scene (Don't change the names of the objects!)
- If you plan to have more than 40 players in your world, duplicate the climbing stations in the same way it is in the package (1 station for 1 player) (It must have the name : "Climbing Station(##)")

- Place climbable objects by using usual colliders and set the layer to Climbing (Use trigger if you want to go throught the object)
- Place swimming water volume (Just create an empty object, add a collider script, enable Is Trigger, change the layer to swimming and set up correctly the volume where you can swim)

#How to disable some parts of the system :
	To disable by default a system, make the Game Object non active(ClimbingSystem, SwimmingSystem or Glider)
	<!!!> If you are disabling a system in game, consider using <system>.Disable<Climbing/Swimming/Gliding>() (Replace <...> by your system) before disabling the Game Object

#To disable stamina, you can hide it by making the object LPlayerInfo(Under LocalPlayerInfo) unactive and put the stamina cost(or stamina per second) to 0 on the three systems)


#Settings :

#Stamina
	 - Maximum stamina (PlayerInfo : Max Stamina) : Default 100
	 - Delay after action to begin regaining stamina (PlayerInfo : Regen Stamina Time) : Default 5
	 - Stamina Recovering Speed (PlayerInfo : Regen Stamina Speed) : Default 20
	 - Cost on the three systems

#Gliding
	- Minimum height from the ground to start gliding (Glider : Gliding Height) : Default 0.5
	- Vertical speed towards the ground when gliding (Glider : Gliding falling rate) : Default 1
	- Maximum speed when gliding (Glider : Max Gliding Speed) : Default 20
	- Gliding Acceleration (Glider : Gliding Acceleration) : Default 20

#Swimming
	- Swimming power multiplicator when you don't have enought stamina (Glider : No Stamina Power Mul) : Default 0.1
	- The acceleration you get by swimming with your hands (Glider : Swimming Power) : Default 0.5
	- The under water drag factor which limits your speed (Glider : Under Water Drag) : Default 20

#Haptics :
	- Amplitude
	- Frequency
	- Duration(Climbing only)


#In game usage :
	- Climbing : Put your hand on a structure and hold the index trigger
	- Swimming : The same for water
	- Gliding : Jump and repress the jump button while in the air, then use your joystick to control the direction

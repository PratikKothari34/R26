# R-26

# Understanding
I understood that I have to decode the UBX data coming from the u-blox GNSS module on-board the rover, and get the GPS data to code an algorithm that plans a path from the start and goal coordinates that are provided by converting these coordinates into grid form and prepare odometry instructions that can traverse the terrian to reach the goal from the start point.

# Thought Process
If I could solve:
1. GPS Decoding - I would decode the recieved UBX message, extract the latitude and longitudnal value which are of integer data type and convert them to decimal data type. By doing this, i get accurate coordinates.
2. Grid Conversion - Since, rover moves in a grid-like pattern, I would map the latitude and longitude coordinates onto a grid, with starting point as (0,0) and the goal or final point relative to the start.
3. Path Planning - On the grid, the rover should take the shortest path to reach the goal from the start. The solution may use some path-finding algorithm.
4. Odometry - Once a path is generated, it should be converted to mechanical movements, like amount of angle to turn and amount time to, move forward. The time can be calculated from wheel radius and RPM
5. Commands Output - Finally, the total time and angle would be written into a result file, so that the rover can read it.

# Where I Got Stuck
I am not able to code in C++. I understood the task given, but I didn't know how to write it in code.

# Use of Help
I used AI to help with certain words like odometry, UBX
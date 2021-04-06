# research

Uitleg over Ros:

`rosrun <package> <executable>` runt een executable, hierbij wordt een node gemaakt met een bepaalde naam. Als je meerdere dezelfde executables wilt runnen moet je met `__name:=<andere naam>` een andere naam meegeven om een nieuwe node te maken.

Met `rqt` kan je services en andere dingen inzien. handige tool!
Met `rqt_console` kan je ook debug berichten zien per node/module. Dan moet je eerst de console openen voordat je andere dingen opent.

Als je `roslaunch turtlebot_gazebo turtlebot_world.launch` uitvoert, kan je de robot via rqt besturen via plugins > robot tools > robot steering. De topic is dan /mobile_base/commands/velocity.

Als je dan een map wilt maken moet je met RViz een map file inladen. Deze moet je eerst maken.
Als je gmapping bezig is, bijvoorbeeld met `roslaunch turtlebot_gazebo gmpaping_demo.launch` kan je de map opslaan. Doe dit in /build zodat het niet mee gepusht wordt.
De map maak je met `rosrun map_server map_saver -f <repository-root>/build/mapfile`.

Nu kan je de map inzien met commando `rviz`, Vervolgens moet je de relevante topics toevoegen met `add` linksonder in het scherm.

De topics om toe te voegen zijn:
  - Map
  - RobotModel
  - LaserScan

(tip: voeg ze toe 'by topic', dan bepaalt RViz voor je welke topics je nodig hebt).

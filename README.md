# Vehicle-collision-avoidance-on-road
Vanet simulation in Netsim :

-> create a .net file in netedit by creating lanes and junctions
-> In the command prompt of the .net file location run the following command to generate a scenario of vechicle simulation
	<path of randomTrips.py in tools folder of sumo> -n <.net.xml file> -r "vehicles.rou.xml" -e 10
-> create a cfg file with the below code:
<configuration>
    <input>
        <net-file value="NETWORK.net.xml"/>
        <route-files value="vechicles.rou.xml"/>
    </input>
    <time>
        <begin value="0"/>
        <end value="10000"/>
        <step-length value="0.4"/>
    </time>
</configuration>

-> open the cfg file in sumo to run the simulation.
-> upload the cfg file in NetSim to simulate the created scenario.
-> create applications between different vechicles with multicast, routing protocols.
-> analyse the forwarding table, throughput graph, performance metrics of the v2v simulation with no collision occuring.

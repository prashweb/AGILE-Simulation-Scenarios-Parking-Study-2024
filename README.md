## Simulation Scenarios for Parking Study

This repository contains the input files and configuration settings used in the study to evaluate the impact of parking placement on through traffic.

### Contents
The repository is structured as follows:

### File Descriptions
- **Network/ Folder**:
  - `network.xml`: Specifies the road network, including all roads, junctions, and lane connections.
  - `parking.xml`: Contains details about parking locations, such as their geographic positions, dimensions, and capacity.
  - `rerouter.xml`: Describes rerouting behavior for vehicles that are searching for empty parking spaces, providing alternative parking options.

- **Traffic-Demand/ Folder**:
  - `router.rou.xml`: Defines the routes for all vehicles in the simulation. This includes:
    - **Through Traffic**: Vehicles that pass through the network without stopping.
    - **Local Traffic**: Vehicles with destinations within the network, including parking spaces.
    - Specifies parking space destinations for local traffic vehicles, enabling analysis of parking demand and its impact on the network.

- **Configs/ Folder**:
  - `config.sumocfg`: Simulation configuration settings.

---

### Instructions
Follow these steps to replicate the simulations:

1. **Install Required Simulation Software**:
   - Install SUMO (https://eclipse.dev/sumo/).

2. **Set Up the Network**:
   - Use the files in the `Network/` folder to define the road network, parking configurations, and rerouting logic.

3. **Load Traffic Demand**: 
   - Change the parking destination in the `routes.rou.xml` file based on the parking placement alternative to be assessed for impact.
   - Change the `vehsPerHour` value in `routes.rou.xml` for each scenario to be simulated.
   - Load the provided traffic demand files from the `Traffic-Demand/` folder into the simulation environment.

4. **Run the Simulation**:
   - Run the simulation using `config.sumocfg` from the `Configs/` folder.
   - Execute the simulation using the software's built-in interface or CLI tools.

---

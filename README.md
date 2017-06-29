# Room Climate Datasets

Room climate data, i.e., temperature and relative humidity, is supected to leak privacy-sensitive information, e.g., the number of occupants in the room or even the activity of these occupants. We evaluated this privacy threat with an experimental study, in which we measured room climate data while one or two occupant(s) performed a pre-defined sequence of tasks.

To encourage further research on IoT privacy issues, we publish our collected sensor data (with groundtruth) as open datasets in this repository. If you refer to these data in a publication, please cite [1].

## Publication

[1] P. Morgner, C. Müller, M. Ring, B. Eskofier, C. Riess, F. Armknecht, Z. Benenson: Privacy Implications of Room Climate Data. To appear in the Procedings of the European Symposium on Research in Computer Security (ESORICS) 2017, Oslo, Norway, September 11-13, 2017. 

## Experimental Design

We collected room climate data at three different locations in form of controlled experiments. The locations are denoted as A, B, and C. 
Each location was eqipped with 3 to 5 room climate sensor nodes at different postions. The floor plan of each location, also including the positions of the sensor nodes, can found in this repository.

For more details about the experimental design and the collected data, please see Section 4 in our publication [1].

## Format of Data

The datasets are split according to their location in the directories `datasets-location_X`.
Each measurement file `room_climate-location_X-measurementYY.csv` contains a series of subsequential room climate measurements. Please note that each measurement file contains measurements of multiple sensor nodes.

Each measurement consists of following information:

`<EID>, <AbsT>, <RelT>, <NID>, <Temp>, <RelH>, <L1>, <L2>, <Occ>, <Act>, <Door>, <Win>`

* `<EID>`: Entry ID
* `<AbsT>`: Absolute timestamp [ms]
* `<RelT>`: Relative timestamp [s]
* `<NID>`: Node ID
* Sensor Data:
  * `<Temp>`: Temperature [°C]
  * `<RelH>`: Relative Humidity [%]
  * `<L1>`: Light Sensor 1 (Wavelength) [nm]
  * `<L2>`: Light Sensor 2 (Wavelength) [nm]
* Groundtruth:
  * `<Occ>`: Number of occupants (0, 1, 2)
  * `<Act>`: Activity of occupant(s) (0 = n/a, 1 = read, 2 = stand, 3 = walk, 4 = work)
  * `<Door>`: State of Door (0 = closed, 1 = open)
  * `<Win>`: State of Window (0 = closed, 1 = open)

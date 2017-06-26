# Room Climate Datasets

[UNDER CONSTRUCTION]

Room climate data, i.e., temperature and relative humidity, is supected to leak privacy-sensitive information, e.g., the number of occupants in the room or even the activity of the occupants. We evaluated this privacy threat with a study, in which we measured room climate data while one or two occupant(s) performed a pre-defined sequence of tasks.

To encourage further research on these issues, we publish our collected sensor data (with groundtruth) as open data sets in this repository. If you use this data in a publication, please reference [1].

## Experimental Setup

We collected room climate data at three different locations in form of controlled experiments. The locations are denoted as A, B, and C. 
The floor plan of each location can found in this repository.

For more details, please see our publication [1].

## Format of Data

Each measurement file contains a series of subsequential room climate measurements. 

Each measurement consists of following information:

* Entry ID
* Absolute timestamp [ms]
* Relative timestamp [s]
* Node ID
* Temperature [°C]
* Relative Humidity [%]
* Light Sensor 1 (Wavelength) [nm]
* Light Sensor 2 (Wavelength) [nm]
* Number of occupants (0, 1, 2)
* Activity of occupant(s) (0 = n/a, 1 = read, 2 = stand, 3 = walk, 4 = work)
* State of Door (0 = closed, 1 = open)
* State of Window (0 = closed, 1 = open)

## Publication

[1] P. Morgner, C. Müller, M. Ring, B. Eskofier, C. Riess, F. Armknecht, Z. Benenson: Privacy Implications of Room Climate Data. To appear in the Procedings of the European Symposium on Research in Computer Security (ESORICS) 2017, Oslo, Norway, September 11-13, 2017. 

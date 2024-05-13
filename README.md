# bgs-dm-meshdp-srv - Data Mesh Data Product

bgs-dm-meshdp-srv is the execution environment for Broda Group
Software's Ecosystem Platform's data products, and is responsible for starting all
components in a Docker Compose run-time environment.

Full documentation is available in in the
[bgs-dm-mesh-doc](https://github.com/brodagroupsoftware/bgs-dm-mesh-doc)
repo.

This application interacts with other applications. You can run
the full set of applications by following instructions in the
[bgs-dm-mesh-doc](https://github.com/brodagroupsoftware/bgs-dm-mesh-doc)
repo.

The remaining sections explain how to Dockerize the application
as well as providing a few developer notes.

## Prerequisites

Docker and Docker Compose must be available.

All Docker images must be available locally or in an
accessible repository.

## Setting up your Environment

Some environment variables are used by various coded and scripts.
Setup your environment as follows (note that "source" is used)
~~~~
source ./bin/environment.sh
~~~~

## Starting the Data Product

Data products are define in directory defined by the "DATA_DIR"
environment variable.  Instances are used to uniquely identify a
data product, and the data product identifier is used to specify
the configuration in DATA_DIR.

Start the data product as follows, using instance 0
and data product "rmi":
~~~~
$PROJECT_DIR/app/startd.sh 0 rmi
~~~~

## License

Use of this source code is governed by an MIT-style
license that can be found in the LICENSE file or at
https://opensource.org/licenses/MIT.

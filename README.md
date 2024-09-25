# tylermwells-TAB-Impementation (Linux Ubuntu)

## Purpose

The sole purpose of this repository is to make a step-by-step installation and running of TAB easier for the ta-expt board. 

## Getting Started

The first step will be to re-flashing the ta-expt board before moving it over to serial setup. You will need to flash it with the flight-401-blr.c. Use the following:

```bash
cd ../../scripts/
source sourcefile.txt
cd ../software/flight-401-blr/
make
st-flash write flight-401-blr.bin 0x8000000
```
## Clone CMU/Tab

The next step will be to clone the repository with the tab protocol. Clone using the following command:

```bash
git clone git@github.com:CMUAbstract/tab.git
```
Once this is done, you will need to move this repository into the development section. This is because in the main repository, the example python code isn't there. To do this, implement the following:

```bash
cd tab/
git checkout develop
```

## Install Python and Dependencies

Next you will need to install python virtual environment and layout the dependencies. This will need to be done in two steps as you will need to shutdown the system. To do this, implement the following:

```bash
sudo apt install python3-venv
sudo usermod -aG dialout $USER
sudo shutdown --reboot now
cd git-repos/tab/python-examples/scripts/
./setup_dependencies.sh
```

## Running Serial Connections to ta-expt

*TODO*

## Activating p3-env and Running Code

Next we will need to source python in order to run the software. In order to do this, run the following command:

```bash
cd /git-repos/tab/python-examples/
source /p3-env/bin/activate
```

When you do this, your command terminal should now have "(p3-env)" down below in the following example:

![alt text](https://github.com/vt-aoe-nanosat-avionics/tylermwells-TAB-Impementation/blob/main/images/p3-env-example.png)

```bash
cd tx/
python3 tx_example.py /dev/ttyUSB0
```
NOTE: ttyUSB0 only implies to Ubuntu/Linux distros. Windows will have a different method of sending the information through the serial terminal. 









# tylermwells-TAB-Impementation

## Purpose

The sole purpose of this repository is to make it easier to implement the TAB protocol. 

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

Next you will need to install python and layout the dependencies. This will need to be done in two steps as you will need to shutdown the system. To do this, implement the following:

```bash
sudo apt install python3-venv
sudo usermod -aG dialout $USER
sudo shutdown --reboot now
cd /git-repos/tab/python-examples/scripts/
./setup_dependencies.sh
```








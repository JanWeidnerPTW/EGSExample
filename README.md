# EGSExample

## Setup a simulation

```
mkdir MySimulation
cd MySimulation
# create the input file say mysimulation.egsinp
# create a README.md file that describes the simulation
```
Try running the simulation:
```
egs_chamber -i mysimulation -p 521icru
```
It will result in an error, because `egs_chamber` by default only sees files in `$EGS_HOME/egs_chamber`.
So we need to link out file as follows:
```
ln $EGS_HOME/egs_chamber/mysimulation.egsinp mysimulation.egsinp
```
Now you can run the simulation.

We also use git for version control. See [here](https://try.github.io) for a tutorial.

```
git init  # create a repo
git add mysimulation.egsinp  # stage changes for commit
git commit -m "one line description of your changes"    # commit changes
```

## Run a simulation
```
egs_chamber -i mysimulation -p 521icru
```

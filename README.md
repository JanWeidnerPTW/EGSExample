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
ln -s mysimulation.egsinp $EGS_HOME/egs_chamber/
```
It is also possible to link all simulations in one command:
```
ln *.egsinp $EGS_HOME/egs_chamber/
```
Now you can run the simulation.

We also use git for version control. See [here](https://try.github.io) for a tutorial.

```
git init  # create a repo in current directory
git add mysimulation.egsinp  # stage changes for commit
git commit -m "one line description of your changes"    # commit changes
```

## Run a simulation
Run simulation:
```
egs_chamber -i mysimulation -p 521icru
```
Run command and record output in a file:
```
egs_chamber -i mysimulation -p 521icru >> myfile.txt
```

## Other useful commands
```shell
egs_view           # visualize geoemtry
diff file1 file2   # show differences between two files
```

#FEniCS

## Version installed:
- FEniCS 2016.1 (gcc 6.1, python 2, openblas)
- FEniCS 2016.2 (gcc 6.1, python 2, openblas)
- FEniCS 2017.1 (gcc 6.1, python 2, openblas)
- FEniCS 2017.2 (gcc 6.1, python 2, openblas)

## Folder structure:
- `build-scripts`: This folder contains the automated script to build fenics using *Hashdist* and *gcc6.1* (`fenics-install-gcc6.1.sh`).
   In addition, it contains symbolic links to the Hashdist profiles to build the different version of FEniCS

- `testing`: A python driver and a jupyter notebook to make sure basic feature of FEniCS are installed correctly. See README for details

- `hashstore_gcc_6.1`: This folder contains the actual binary files, headers, and python packages built by Hashdist with the `gcc 6.1` compiler for all version of FEniCS.

- `gcc_6.1`: This folder and its subfolders contain the bash scripts the user should source to load a specific version of FEniCS. It also contain a copy of the Hashdist profile
   and the Hashstack git commit hash used to built that specific version for future reference.

## How to use FEniCS

- To use FEniCS 2016.1 (gcc 6.1, python 2, openblas)
```
source /opt/apps/ossw/applications/fenics-h/gcc_6.1/2016.1/fenics
```

- To use FEniCS 2016.2 (gcc 6.1, python 2, openblas)
```
source /opt/apps/ossw/applications/fenics-h/gcc_6.1/2016.2/fenics
```

- To use FEniCS 2017.1 (gcc 6.1, python 2, openblas)
```
source /opt/apps/ossw/applications/fenics-h/gcc_6.1/2017.1/fenics
```

- To use FEniCS 2017.2 (gcc 6.1, python 2, openblas)
```
source /opt/apps/ossw/applications/fenics-h/gcc_6.1/2017.2/fenics
```


*NOTE*: This bash script will purge all the loaded module, and load c7 and gcc/6.1.
*NOTE*: To source different version of fenics in the same terminal window may lead to unexpected behaviors.

## Just in time compiler cache
The folders `$HOME/.fenics_cache/$HOSTNAME/instant/$PROFILE` and `$HOME/.fenics_cache/$HOSTNAME/dijitso/$PROFILE`
will be used to store the cache for the FEniCS just in time compiler. 
Here, `$PROFILE` expands to a unique identifier for the specific version of FEniCS that was loaded.

# learn-fenics

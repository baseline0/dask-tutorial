## quick notes

verify installer hash on ubuntu
```bash
sha256sum Anaconda3-2023.09-0-Linux-x86_64.sh 
```

this is orig as per README
```bash
conda install -c conda-forge ipycytoscape jupyterlab python-graphviz matplotlib zarr xarray pooch pyarrow s3fs scipy dask distributed dask-labextension
```

also needed? not sure. try to remove and repeat w only python-graphviz
```bash
conda install -c anaconda graphviz
```

### solver

solving was taking a looooooong time. seems libmamba is preferred but not default?


```bash
conda install -n base conda-libmamba-solver
conda config --set solver libmamba
```



### tutorial changes as they occurred

could not upload s3 file until msgpack was updated as follows:

```bash
conda install -c conda-forge msgpack-python==1.0.5
```


```bash
conda install jupyterlab
conda install dask distributed -c conda-forge
```


run in separate terminal:
```bash
dask scheduler
```

 ---

got conflict with use of default port. seems to move ok. see new port in jupyter or commandline.

see what else is running on port:8787

```
sudo netstat -nlp | grep :8787
```
 


# DIAD laminography demo for users

Uses `pixi` as the package manager (https://confluence.diamond.ac.uk/display/~qps56811/Using+Pixi+for+Python+Environment+Management+at+Diamond)

```
git clone https://github.com/DIAD-beamline/diad-lamino-recon-notebooks
cd diad-lamino-recon-notebooks
pixi install
```
Now you're ready.
```
pixi run jupyter lab
```


## If you don't have `pixi` set up:

Install pixi in your science area (only need to do this once):

### Create pixi directory in science area (replace fedid with your FedID)
`mkdir -p /dls/science/users/$FEDID/.pixi`
 
### Install pixi
`curl -fsSL https://pixi.sh/install.sh | PIXI_HOME=/dls/science/users/$FEDID/.pixi bash`
 
### Add to PATH in ~/.bashrc
`echo "export PATH=\"/dls/science/users/$FEDID/.pixi/bin:\$PATH\"" >> ~/.bashrc`
 
### Set up cache directory in science area to avoid home quota issues
```
mkdir -p /dls/science/users/$FEDID/cache/rattler
echo "export RATTLER_CACHE_DIR=\"/dls/science/users/$FEDID/cache/rattler\"" >> ~/.bashrc
 
source ~/.bashrc
```

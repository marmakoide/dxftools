# dxftools

This script allows to manipulate 2D DXF files

* viewing the content of a file
* computing an offset (for example, to take in account the kerf of a laser cutter)

## Getting Started

### Prerequisites

You will need

* Python 2.7 or above
* [Numpy](http://www.numpy.org)
* [Shapely](https://github.com/Toblerity/Shapely)
* [Click](https://click.palletsprojects.com)
* [Matplotlib](https://matplotlib.org)

Additionally, you might want to have [virtualenv](https://pypi.org/project/virtualenv/), 
although it's not mandatory.

### How to install it

You can create an independent environment with all the required packages
downloaded for you update, using *virtualenv*

Create a virgin Python environment

```
virtualenv env
```


Enter that environment

```
source ./env/bin/activate
```

Download the dependencies

```
pip install -r requirements.txt
```

### Displaying the content of a DXF

```
./dxftools view myfile.dxf
```

As of now, be warned that the display is not automatically adjusted to fit the
drawing, the script blindly trust the bounding box set in the DXF file.

### Offseting a DXF

```
./dxftools offset --offset=0.2 input.dxf output.dxf
```

This command will take *input.dxf*, compute an outer offset of 0.2 units, and
write the result to *output.dxf*. If you want an inner offset, give a negative
number.



## Authors

* **Alexandre Devert** - *Initial work* - [marmakoide](https://github.com/marmakoide)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details



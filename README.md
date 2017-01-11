Test packages installation
====

$ wget https://raw.githubusercontent.com/fchollet/keras/master/examples/mnist_mlp.py

$ python mnist_mlp.py

Test application installation
====

$ cd visual-qa/scripts
$ sh get_started.sh


For ubuntu 15.10
====

1.
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.10.0-cp27-none-linux_x86_64.whl
$ sudo pip install $TF_BINARY_URL

2.

hdf5:
see: https://support.hdfgroup.org/ftp/HDF5/releases/hdf5-1.10/hdf5-1.10.0-patch1/src/unpacked/release_docs/INSTALL

$ wget https://support.hdfgroup.org/ftp/HDF5/releases/hdf5-1.10/hdf5-1.10.0-patch1/src/hdf5-1.10.0-patch1.tar
$ gunzip < hdf5-X.Y.Z.tar.gz | tar xf - or tar zxf hdf5-X.Y.Z.tar.gz
$ cd hdf5-X.Y.Z
$ ./configure --prefix=/usr/local/hdf5 <more configure_flags>
or ./configure --prefix=/usr/local/hdf5 --enable-fortran \
              --enable-cxx --with-szlib=PATH_TO_SZIP
$ make
$ make check                # run test suite.
$ make install
$ make check-install        # verify installation.


$ export HDF5_DIR=/usr/local/hdf5
$ pip install h5py

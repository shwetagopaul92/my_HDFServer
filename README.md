
#HDF SERVER

#Introduction
HDF Server is a Python-based web service that can be used to send and receive HDF5 data using an HTTP-based REST interface.

#SETUP 

1.Local Installation: 

Python packages required:
* NumPy 1.10.4 or later
* h5py 2.5 or later
* tornado 4.0.2 or later
* watchdog 0.8.3 or later
* requests 2.3 or later (for client tests)

a.) Install Anaconda 
```{}

  conda create -n h5serv python=2.7 h5py tornado requests pytz
  pip install watchdog
  source activate h5serv
  
```

b.) Clone the hdf5-json project:
```{}

  git clone https://github.com/HDFGroup/hdf5-json.git
  cd hdf5-json/
  python setup.py install
  
```

c.) Clone the h5serv project:
```{}

 git clone https://github.com/HDFGroup/h5serv.git
 cd h5serv/server/
 python app.py
 
```
The server would start running. 
This would be indicated by the output - Starting event loop on port: 5000

2. AWS Instance

a.) Launch an AWS Instance

b.) Perform the above mentioned steps to install the HDF server in the instance. 

c.) Run the server

```{}

  cd h5serv/server
  python app.py
  

```

The server would start running. 
This would be indicated by the output - Starting event loop on port: 5000


#Verification 

To verify that the h5serv was installed correctly: 

1. Open a new terminal/ Launch the AWS instance again

2. Run Anaconda command prompt

```{}

  source activate h5serv
  cd h5serv/test
  python testall.py
  

```

This would run a number of tests to verify the installation. 

# cropclassification
This is a collection of scripts that can help to classify crops using Sentinel data.

## Installation manual

1. As google earth engine is used to get the Sentinel data for the classification, you will need a google account 
that has google earth engine access enabled. So go to https://earthengine.google.com/ and click "Sign up" at the 
top right if you haven't used google earth engine yet.

2. As the scripts are written in Python, you need to use a package manager to be able to install the packages the 
scripts depend on. The rest of the installation manual assumes you use anaconda. 
You can install this from https://conda.io/docs/user-guide/install/index.html

3. Once you have anaconda installed, you can open a terminal window and install the dependencies in one of the following ways:

   1. Use the requirements.txt file
      1. navigate to the directory where you downloaded/cloned the scripts to, by doing eg. 
	  ```
	  cd c:\temp\cropclassification
	  ```
      2. run the following command: 
	  ```
	  conda env create -n cropclassification --file cropclassification.yml
	  ```

   2. Install the dependencies manually
      1. Create a new conda environment
      ```
	  conda create --name cropclassification python=3.6 anaconda`
      conda activate cropclassification
	  ```
      2. Install the dependencies for the crop classification scripts:
	  ```
      conda install geopandas
	  ```

      3. Install the python earth engine API
      ```
	  conda install -c conda-forge earthengine-api
	  ```
      4. Install scikit-learn
      ```
	  conda install scikit-learn
	  ```
      5. Install google-api-python-client
      ```
	  conda install -c conda-forge google-api-python-client
	  ```
      6. I use spyder to edit my scripts. Recently after I installed geopandas, Spyder from the root environment doesn't work anymore and I need to install it here as well. If you use another editor, you can use that of course.
      ```
	  conda install spyder
	  ```
4. When you want to download data from google earth engine, this data is placed on your google drive. For the scripts 
to be able to download this data they scripts need (read-only) access to your google drive. Follow the steps explained 
on the following page, but skip step 2 as it will be installed already and using pip and conda together can break some 
things: 
https://developers.google.com/drive/api/v3/quickstart/python.

5. You can now open the scripts in eg. spyder, and check out especially main_run.py and global_settings.py. You need to
update those to match your environment, eg. set the paths as you want them,...

6. Now run `main_run.py` to start a crop classification...

## Sample data

Sample data can be downloaded from the following location. If you don't change the default paths in the scripts in needs to be put in the directory C:\temp\CropClassification\InputData
https://drive.google.com/open?id=1eN9cBcWyvM0msNMCD6nivcGuZfYyqV5q

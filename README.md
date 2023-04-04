# AMIRA custom modules
Python scripts developped for integration as custom modules in Amira-Avizo (Thermo Fisher Scientific Inc.). The `.pyscro` file is a Python script written with the Thermo Fisher Python API. The `.rc` file is a TCL script which makes the module available for Amira-Avizo.

## How to install?
1. Drop a pair of `.pyscro`/`.rc` files in the `python_script_objects` folder of your Amira-Avizo installation, e.g. `C:\Program Files\Thermo Scientific Amira-Avizo3D 2022.2\share\python_script_objects` for version 2022.2 on Windows 10
2. Restart the Amira-Avizo software.
3. In the Project View, right-click and pick 'Create Object...'
4. The new module is available under the 'Custom' category.

## Available scripts

### `CreateROI.pyscro` | `PythonCreateROI.rc`
Create orthogonal ROI Boxes that cross at the defined coordinate and span through the whole volume.

### `ComputeProfile.pyscro` | `PythonComputeProfile.rc`
Compute profile from a ROI Box along the chosen axis then save the values to a `.csv` file.

Three modes exist:
1. Mean profile along the chosen axis.
2. Gradient (first derivative) of mean profile
3. Mean of the gradients of profiles (used for testing only)

### `ExportHistogram.pyscro` | `PythonExportHistogram.rc`
Compute histogram of a volume and save the values to a `.csv` file. This does not handle ROI Boxes, thus you would need to use the **Extract Subvolume** module and choose the subvolume as input for the custom module.

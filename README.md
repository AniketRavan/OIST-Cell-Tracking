# OIST-Cell-Tracking
This is a semi-supervised tracking algorithm written to track cells in phase contrast images using MATLAB's R2015a version. Images undergo binary classification based on pixel intensity and local standard deviation of pixel values. A Support Vector Machine classifier is used for this step. The classifier is automatically trained in every frame using information between successive frames. 
Please note that the algorithm is written for single cell studies and only independent cells are tracked. The rate at which images are captured has to be above a certain minimum. The algorithm may give erroneous results if the distance traveled by any cell between two frames is greater than its own dimension. 

# Using the Software
Tracking is initiated by running the 'CodeForTracking' script in the repository. Once the required image files are selected, the
user is expected to click on the (independent) cells to be tracked. Cells that happen to develop adhesion sites between each other in successive frames are ignored in future events. The user can pause and re-assign the cells to be tracked. Information regarding the displacements in every frame is stored in MATLAB cell arrays 'theta' and 'distance'.

#Plausible Improvements
Automatically resume tracking of independent cells that were ignored in a previous frame.

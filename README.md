
1. **Source File Import:** Import the model export files into the Construct 3 project file tree. A complete set of three formats is required: the skeleton structure file (`.json`), the atlas coordinates file (`.txt`), and the texture map file (`.png`).
2. **Object Declaration:** Create a new *Spine* object type class within the workspace (Layout).
3. **Property Mapping:** In the *Properties* panel, assign the imported reference files to the corresponding parameters of the new class:
* *Skeleton data* parameter $\rightarrow$ `.json` file
* *Atlas data* parameter $\rightarrow$ `.txt` file
* *Texture* parameter $\rightarrow$ `.png` file

4. **Architecture Integration:** Add the newly created object class to the `SpineFamily` group. This operation connects the object to the implemented event sheet logic.
5. **Initialization State Clearance:** Locate the `Initial animation` text field in the object's *Properties* panel. The value of this parameter must be cleared (the field must remain completely empty). The presence of any string in this field prior to the completion of the asynchronous AJAX request results in a critical WebGL pipeline error.
6. **Reference Instance Allocation:** Place exactly one instance of the new object within the workspace of the startup layout. Define the instance position vector (X, Y) outside the camera projection bounds (e.g., `X: -2000`, `Y: -2000`).

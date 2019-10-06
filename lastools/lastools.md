## lstools

* http://lastools.org/
* https://github.com/LAStools/LAStools

![overview](lastools_img/overview.png)

render only ground data

![ground only](lastools_img/render_ground_only.png)

triangulate a DTM???

![tiangulation](lastools_img/triangulate.png)

![triangulation result](lastools_img/triangulate_result.pmg)
![triangulation result](lastools_img/triangulate_result_no_points.png)


better use batch files


### first project

copy stuff to folder

![should look like this](lastools_img/project_folder.png)

open lasinfo

![should look like this](lastools_img/project_add_stuff.png)

![should look like this](lastools_img/project_keep_only_class_2.png)

![should look like this](lastools_img/project_specify_output_file.png)

![should look like this](lastools_img/project_run.png)

![promt](lastools_img/project_run_prompt.png)

```
lasinfo -cpu64 -lof file_list.9544.txt -keep_classification 2 -otxt -odix "_lasinfo"
```

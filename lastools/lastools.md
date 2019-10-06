lastools
========

* http://lastools.org/
* https://github.com/LAStools/LAStools

![overview](lastools_img/overview.png)

render only ground data

![ground only](lastools_img/render_ground_only.png)

### triangulation

![tiangulation](lastools_img/triangulate.png)

![triangulation result](lastools_img/triangulate_result.png)

![triangulation result](lastools_img/triangulate_result_no_points.png)


better use batch files


### retrieve meta data 

copy stuff to folder

![should look like this](lastools_img/project_folder.png)

open lasinfo and add files

![should look like this](lastools_img/project_add_stuff.png)

drop everything not class 2 (ground)

![should look like this](lastools_img/project_keep_only_class_2.png)

use meaningful file naming to prevent intense searching afterwards

![should look like this](lastools_img/project_specify_output_file.png)

running the configuration should promt console command, click start to really run

![should look like this](lastools_img/project_run.png)

![promt](lastools_img/project_run_prompt.png)

```
lasinfo -cpu64 -lof file_list.9544.txt -keep_classification 2 -otxt -odix "_lasinfo"
```

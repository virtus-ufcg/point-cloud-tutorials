# Point Cloud Library Tutorials

* [Link](http://pointclouds.org/documentation/tutorials)

Install APT dependencies before compile and run each tutorial for Ubuntu 16.04 x64:

```
./install.sh
```

## Tutorials:

- [Plane model segmentation](http://pointclouds.org/documentation/tutorials/planar_segmentation.php)
```
rm -rf planar_segmentation/build
mkdir planar_segmentation/build && cd planar_segmentation/build
cmake .. && make
chmod +x planar_segmentation
./planar_segmentation
```

- [Cylinder model segmentation](http://pointclouds.org/documentation/tutorials/cylinder_segmentation.php#cylinder-segmentation)
```
rm -rf cylinder_segmentation/build
mkdir cylinder_segmentation/build && cd cylinder_segmentation/build
cmake .. && make
chmod +x cylinder_segmentation
cp ../table_scene_mug_stereo_textured.pcd .
./cylinder_segmentation
```

- [The CloudViewer](http://pointclouds.org/documentation/tutorials/cloud_viewer.php)
```
rm -rf cloud_viewer/build
mkdir cloud_viewer/build && cd cloud_viewer/build
cmake .. && make
chmod +x cloud_viewer
cp ../my_point_cloud.pcd .
./cloud_viewer
```

- [How to visualize a range image](http://pointclouds.org/documentation/tutorials/range_image_visualization.php)
```
rm -rf range_image_visualization/build
mkdir range_image_visualization/build && cd range_image_visualization/build
cmake .. && make
chmod +x range_image_visualization
cp ../ism_train_wolf.pcd .
./range_image_visualization ism_train_wolf.pcd
```

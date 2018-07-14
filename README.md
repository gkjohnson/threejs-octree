# threejs-octree
A rough octree implementation to support frustum culling and raycasts in complex THREE.js scenes.

## TODO
- Max depth is needed in case there are a bunch of objects right on top of eachother
- Consider adding an optimization using SAH and constricting the bounding boxes a a bit more
- Provide an option for iteratively flushing all pending inserts because this can be expensive on cast operations
- Raycasts can be a bit slow when the tree is large. This seems due to a lot of objects not being pushed down into leaves that are straddling an octant boundary.
- Add, update, and remove operations are all delayed at the moment as well as the objects being pushed down into the tree -- we shouldn't need both (or either? Remove them?)
- Optimize object removal.
- Use something like an SAH algorithm to decide when to split.
- Shrink the bounds to a size that optimially constrains the child objects?

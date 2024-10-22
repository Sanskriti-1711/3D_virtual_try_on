# 3D_virtual_try_on

With the rapid growth of e-commerce and online fashion retail, there has been a
rising demand for accurate virtual try-on systems that let customers see how clothes
fit on a 3D human body are in more demand due to the explosive expansion of e-
commerce and online fashion retail. Our goal in this research is to match garment
models onto human body meshes recreated from 2D pictures using
a 3D virtual try-on system. The SMPL model, Multi-Scale Iterative Closest Point
(ICP), Point-to-Plane ICP, and the Geometric Correspondence Matching Network
(GCM Net) are among the approaches that are examined and assessed in our work.
The SMPL model1 is leveraged to generate human body meshes from pose and
shape parameters. However, the model shows limitations in generalizing to unseen
human meshes, such as those produced by PIFuHD2, particularly when applied to
unseen poses and shapes. Both Multi-Scale ICP3 and Point-to-Plane ICP4 were
evaluated for aligning garment meshes to human body meshes. These techniques
achieved high accuracy on seen human meshes but faced substantial challenges
when generalizing to unseen data, resulting in a noticeable drop in fitness scores
and increased RMSE (Root Mean Squared Error).

GCM Net5 is used to address these limitations, a neural network designed
to handle non-rigid deformations and establish geometric correspondences between
the garment and body meshes. GCM Net demonstrated superior generalization
to unseen data compared to ICP-based methods, especially on PIFuHD-generated
human meshes. However, the performance of GCM Net also degraded at finer scales,
indicating that further optimization and training data may be necessary to improve
its accuracy in handling complex deformations and variations in garment draping.
The results reveal that traditional rigid alignment methods, such as ICP, strug-
gle with non-rigid deformations and unseen human meshes, while GCM Net offers a
more flexible and robust approach to garment fitting. Nonetheless, GCM Net still
requires additional improvements to achieve high accuracy at finer mesh resolutions.
Future work will focus on hybrid approaches that combine the strengths of ICP for
coarse alignment with GCM Net for finer, non-rigid adjustments, as well as incor-
porating physics-based models for more realistic garment simulation. Additionally,
data augmentation techniques and transfer learning could be explored to further
enhance the generalization capabilities of the system.

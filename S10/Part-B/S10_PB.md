## **PART - B**

### **Aim**

- ✅ Download coc.txt file. Learn how COCO object detection dataset's schema is. 
- ✅ Identify these things for this dataset:
  - readme data for class distribution (along with the class names) along with a graph 
  - Calculate the Anchor Boxes for k = 3, 4, 5, 6 and draw them.
  - Share the calculations for both via a notebook uploaded on your GitHub Repo

### **Graph for Class Distribution**

There are 80 categories in the provided dataset and its distribution is shown below:
![graph_for_class_dis.PNG](images-B/graph_for_class_dis.PNG)

### **Bounding Box**

A bounding box is a rectangle that surrounds an object, that specifies its position, class and confidence(how likely it is to be at that location). Bounding boxes are mainly used in the task of object detection, where the aim is identifying the position and type of multiple objects in the image.          
![bounding_box.PNG](images-B/bounding_box.PNG)


### **Anchor Box and K-values**

Anchor boxes are nothing but template bounding boxes. Object detection models utilize the anchor boxes to make beter bounding box predictions. 

**Anchor Box Cluster**       
![anchorbox_cluster.PNG](images-B/anchorbox_cluster.PNG)

**Anchor Boxes for different K values**

When K = 3    
![anchor_3.PNG](images-B/anchor_3.PNG)   

When K = 4    
![anchor_4.PNG](images-B/anchor_4.PNG)     

When K = 5     
![anchor_5.PNG](images-B/anchor_5.PNG)     

When K = 6  
![anchor_6.PNG](images-B/anchor_6.PNG)     

## Uni project
## Innovative Parking Analysis: Curbs Detection, Drone-Assisted Parking Insights, and Video Sign Recognition from Images


**Description:**

Step into the world of innovation and creativity as we unravel the secrets of parking analysis, traffic monitoring, and road safety enhancements. Our project is  combination of unique ideas, blending a homemade quadcopter, iPhone LiDAR sensor for height maps, and YOLO for curb, sign, and car detections.

Embark on an extraordinary journey into parking behaviors, vehicle positioning, and traffic sign recognition like never before.


**Key Features:**

**LiDAR curb detection:** Harness the potential of iPhone LiDAR to reimagine curbs as intricate height maps. This groundbreaking approach transforms curbs into data-rich visuals, fostering urban planning and strategic parking allocation.

**Parking analysis:** Our homemade quadcopter, coupled with YOLO and QuickHull algorithms, soars above to assess parking alignment against our dataset. Real-time parking evaluations, streamlined vehicle placements, and valuable insights empower optimized parking management.

**Road signs detection:** Our phone camera navigates the urban landscape, capturing street marks and signs with precision. Through advanced recognition, we uncover vital traffic guidelines, enhancing road safety.


**Detailed description of transferring LiDAR data into height maps:**

Explore our code that forms the backbone of our innovative project, combining Lidar technology and creative algorithms to revolutionize parking analysis and road safety. Here's a quick overview of what our code does:

- `extractVertexes(filePath)`: This function loads 3D models from file paths and extracts vertex positions, essential for subsequent analysis.

- `Draw2DImage(vertexPositions)`: Visualize 2D images by plotting vertex positions on a scatter plot, showcasing parking patterns and positions.

- `Draw3DGraph(vertexPositions)`: Create a 3D model visualization, offering a holistic view of parking arrangements, complete with dynamic color mapping.

- `buildHeatmapImage(vertexPositions)`: Generate heatmap images from 3D vertex positions, converting them into data-rich visuals for urban planning and allocation.

- `buildGrayscaleImage(vertexPositions)`: Transform 3D vertex positions into grayscale images, providing insights into height variations of road.

- `makeLabelAndSave(vertexPositions)`: Build grayscale images and save them, capturing and preserving parking insights for future analysis.

- `findNeighbours(vertex)`: Utilize Delaunay triangulation to identify neighboring vertices for each vertex, an essential step for further processing.

- `decimateVertexes(vertices, threshold)`: Reduce vertex count based on specified thresholds, optimizing processing speed while preserving essential data.


**Detailed description of our data stream protocol using Kafka and Redis:**

- `Pro_video.py`: The script, named Pro_video.py, serves as the producer for the video processing and streaming pipeline. It captures frames from a video source, utilizes Redis for frame storage, and sends notifications about new frames via Kafka.
  
- `Con_pro_detection.py:` The script, named Con_pro_detection.py, plays the role of the consumer in the detection process. It subscribes to Kafka notifications, extracts frames from Redis, performs object detection with YOLO, and communicates detection results back via Kafka.

- `con_visualization.py:` The script named con_visualization.py handles visualization tasks by overlaying detected object information on video frames. It subscribes to Kafka messages containing detection details, processes these details, and adds visual annotations to frames. It allows us to see how detection results are rendered for end-user observation.
 


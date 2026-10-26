# Drone and Bird Flock Tracking with YOLO, Kalman Filtering, and Relative 3D Depth

A computer vision prototype for detecting and tracking drones and birds in video, grouping bird detections into flocks, predicting object motion, and visualizing approximate 3D trajectories using monocular relative depth.
The project combines YOLO object detection, multi-object association, Kalman filters, and Video Depth Anything Small. An interactive Plotly dashboard synchronizes annotated 2D footage with relative 3D tracks and short-horizon motion predictions.

# Features
- Drone and bird detection: Train and run a YOLO-based detector on custom drone/bird video data.
- Bird flock analysis: Cluster nearby bird detections with DBSCAN and maintain persistent flock associations across frames.
- Multi-object tracking: Associate detections over time, maintain object tracks, and export annotated video and CSV tracking data.
- 2D motion estimation: Use Kalman filtering to smooth trajectories and predict future image-plane positions.
- Monocular depth estimation: Generate frame-level relative depth maps using Video Depth Anything Small.
- Depth-aware tracking: Associate depth values with tracked objects and smooth depth measurements with a Kalman filter.
- Relative 3D visualization: Combine image-plane positions with relative depth and display observed paths and a one-second linear motion extrapolation.
- Synchronized dashboard: Select a track and inspect its motion alongside the corresponding 2D video.

# Youtube Video
https://www.youtube.com/watch?v=95mWD1Y4PtE

# Dashboard
The dashboard shows annotated 2D footage beside a Plotly 3D plot. Choose a tracked object to see its recent trajectory, its extrapolated path up to one second ahead, and an estimated depth trend. The HTML file includes embedded video and tracking data; it can therefore be relatively large.
Open synchronized_2d_3d_dashboard.html in a browser. Use the track selector and video controls to inspect synchronized 2D and relative 3D tracking. Plotly is loaded from a CDN, so viewing the dashboard requires network access to that script unless it is bundled locally.


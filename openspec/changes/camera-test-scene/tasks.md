## 1. Create Camera Test Scene

- [ ] 1.1 Create `scenes/camera_test.tscn` with Node2D root and Camera2D child
- [ ] 1.2 Set initial camera position to center of viewport (640, 360)
- [ ] 1.3 Save scene file with proper formatting

## 2. Create Camera Test Controller Script

- [ ] 2.1 Create `scripts/camera_test.gd` extending Node2D
- [ ] 2.2 Add @export variables for camera speed, zoom speed, and follow smoothing
- [ ] 2.3 Attach script to camera_test.tscn root node

## 3. Implement Camera Movement Controls

- [ ] 3.1 Implement WASD keyboard input for camera position adjustment
- [ ] 3.2 Implement Q/E keys for zoom in/out
- [ ] 3.3 Ensure camera respects project viewport boundaries

## 4. Implement Visual Debugging Aids

- [ ] 4.1 Implement _draw() method to render grid lines across visible area
- [ ] 4.2 Implement boundary marker drawing when camera limits are set
- [ ] 4.3 Ensure grid scales appropriately with camera zoom

## 5. Implement Camera Follow Testing

- [ ] 5.1 Add movable target object (Sprite2D or simple shape) to scene
- [ ] 5.2 Implement arrow key controls to move target object
- [ ] 5.3 Add toggle mechanism (e.g., F key) to enable/disable camera follow
- [ ] 5.4 Implement smooth camera follow when follow mode is enabled
- [ ] 5.5 Ensure camera remains stationary when follow mode is disabled

## 6. Testing and Verification

- [ ] 6.1 Run scene and verify it loads without errors
- [ ] 6.2 Test all keyboard controls work as expected
- [ ] 6.3 Verify grid and boundary markers are visible
- [ ] 6.4 Test camera follow with target object movement

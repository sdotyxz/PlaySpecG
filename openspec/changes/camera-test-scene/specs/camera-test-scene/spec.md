## ADDED Requirements

### Requirement: Camera test scene provides isolated testing environment
The system SHALL provide a standalone scene for camera behavior testing that loads independently from the main game scene.

#### Scenario: Scene loads successfully
- **WHEN** the user opens `scenes/camera_test.tscn`
- **THEN** the scene displays without errors and shows a Camera2D node ready for testing

### Requirement: Visual debugging aids are present
The system SHALL display visual grid lines and boundary markers to help verify camera positioning and limits.

#### Scenario: Grid is visible
- **WHEN** the camera test scene is running
- **THEN** a grid is drawn across the visible area to help judge distances and positions

#### Scenario: Boundary markers show limits
- **WHEN** the camera test scene is running
- **THEN** boundary markers indicate the configurable camera limits (if set)

### Requirement: Camera properties are adjustable at runtime
The system SHALL allow modification of camera properties (position, zoom, limits, follow smoothing) during scene execution.

#### Scenario: Adjust camera zoom
- **WHEN** the user presses Q or E keys
- **THEN** the camera zoom level increases or decreases accordingly

#### Scenario: Move camera position
- **WHEN** the user presses WASD keys
- **THEN** the camera position moves in the corresponding direction

### Requirement: Camera follow behavior can be tested
The system SHALL include a movable target object that the camera can optionally follow to test follow mechanics.

#### Scenario: Enable camera follow
- **WHEN** the user enables follow mode and moves the target with arrow keys
- **THEN** the camera smoothly follows the target object

#### Scenario: Disable camera follow
- **WHEN** the user disables follow mode
- **THEN** the camera remains stationary regardless of target movement

## Why

We need a dedicated test scene to verify camera behavior, positioning, and movement mechanics in isolation from gameplay logic. This will enable rapid iteration on camera systems without loading the full game scene and provide a sandbox for testing camera edge cases.

## What Changes

- Create `scenes/camera_test.tscn` - A standalone test scene with visual markers for camera bounds
- Create `scripts/camera_test.gd` - Controller script for camera testing with debug visualization
- Add configurable camera properties (zoom, position limits, follow smoothing) that can be adjusted at runtime
- Add visual grid and boundary markers to help verify camera positioning
- **BREAKING**: None

## Capabilities

### New Capabilities
- `camera-test-scene`: A dedicated testing environment for camera behavior validation with interactive controls and visual debugging aids

### Modified Capabilities
- (none)

## Impact

- New scene file: `scenes/camera_test.tscn`
- New script file: `scripts/camera_test.gd`
- No changes to existing main scene or core game logic
- Development/testing workflow improvement only

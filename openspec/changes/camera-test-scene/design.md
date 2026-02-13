## Context

The PlaySpecG project is a Godot 4.6 game project currently using a basic Camera2D in the main scene. For effective camera system development, we need an isolated test environment that allows developers to verify camera behaviors (zoom, panning, limits, smoothing) without the overhead of loading the full game scene.

Current state: Single main scene with basic Camera2D at fixed position (640, 360)

## Goals / Non-Goals

**Goals:**
- Provide an isolated test scene for rapid camera iteration
- Enable runtime adjustment of camera properties for quick testing
- Include visual debugging aids (grid, boundaries) for clear position verification
- Support testing of common camera patterns (follow, limits, zoom)

**Non-Goals:**
- No integration with actual game entities or gameplay logic
- No persistent save/load of camera settings
- No automated testing framework integration

## Decisions

**Decision: Use Node2D root with Camera2D child**
- Rationale: Matches the pattern used in main.tscn for consistency
- Alternative considered: Control node for UI-based testing, but Node2D is more appropriate for 2D game camera testing

**Decision: Implement keyboard controls for camera manipulation**
- WASD for camera position, Q/E for zoom, arrow keys for testing camera limits
- Rationale: Simple, no additional dependencies, works in editor
- Alternative considered: UI sliders, but keyboard is faster for quick iteration

**Decision: Draw debug visualization using _draw() method**
- Rationale: Native Godot drawing, no external assets needed, always visible
- Alternative considered: Sprite2D markers, but drawing is more flexible for grids

**Decision: Include a movable target object**
- Rationale: Allows testing camera follow behavior with a controllable subject
- The target can be moved with arrow keys while camera follows

## Risks / Trade-offs

- [Risk] Debug visualization may clutter view when zoomed out far → Mitigation: Grid scales with zoom, can toggle visibility
- [Risk] Keyboard controls may conflict with editor shortcuts → Mitigation: Only active when scene is running

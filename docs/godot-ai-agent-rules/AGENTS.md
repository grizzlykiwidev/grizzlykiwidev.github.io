# AGENTS.md (Godot 4 project)

Instructions for AI coding agents (Codex, Cursor, Claude Code, Copilot, Windsurf).
Free template from https://grizzlykiwidev.github.io/godot-ai-agent-rules/ . Edit the bits in <angle brackets>.

## Project
- Engine: Godot <4.x> (GDScript). Godot 4 syntax only. Never write Godot 3 code.
- Main scene: <res://scenes/main.tscn>
- Run: `godot --path .`

## Layout
- `scenes/`: .tscn scenes, one folder per feature
- `scripts/`: .gd scripts, named after their scene (snake_case)
- `resources/`: .tres data files (items, enemies, levels)
- `autoload/`: global singletons. Don't add new ones without asking.
- `addons/`: third-party plugins. Don't edit.

## Godot 3 -> Godot 4 (use the right column)
| Godot 3 (wrong) | Godot 4 (use) |
|---|---|
| `export var speed = 200` | `@export var speed := 200.0` |
| `onready var x = $X` | `@onready var x: Node2D = $X` |
| `yield(obj, "signal")` | `await obj.signal` |
| `connect("pressed", self, "_on_pressed")` | `pressed.connect(_on_pressed)` |
| `emit_signal("died")` | `died.emit()` |
| `KinematicBody2D` / `Spatial` | `CharacterBody2D` / `Node3D` |
| `move_and_slide(velocity, Vector2.UP)` | set `velocity`, then `move_and_slide()` |
| `tool` | `@tool` |
| `instance()` | `instantiate()` |

## Conventions
- Static typing everywhere: `var hp: int = 100`, `func take_damage(amount: int) -> void:`.
- snake_case for files, functions and variables; PascalCase for `class_name` and node names.
- "Call down, signal up": parents call children; children emit signals. No `get_parent()` chains.
- Use `%UniqueName` or `@export` node references instead of long `$A/B/C` paths.
- Movement in `_physics_process(delta)`. Use Input Map actions, never raw keycodes.
- Game data lives in `Resource` subclasses (.tres), not dictionaries.

## Check your work
- After every change run: `godot --headless --path . --quit` <or your test command, e.g. tools/check.sh>
- Fix every error or warning it prints before saying you're done.

## Don't
- Hand-edit .tscn or .tres files beyond trivial changes. Describe the editor steps instead.
- Rename or remove autoloads, input actions or exported properties without asking.
- Change project.godot or export_presets.cfg without asking.
- Commit or print anything from export_credentials.cfg or other secrets.

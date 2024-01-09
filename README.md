# Godot Style Guide
Heavily inspired by the [Airbnb Javascript Style Guide](https://github.com/airbnb/javascript) and [Michael Allar’s UE5 Style Guide](https://github.com/Allar/ue5-style-guide?tab=readme-ov-file#structure)


# 1. Asset Naming Conventions

## 1.1 Base Asset Name - `prefix_baseassetname_variant_suffix`

| Type       | Style       |
| --------   | -------     |
| Nodes      | PascalCase  |
| Folders    | snake_case  |
| Scenes     | snake_case  |
| Scripts    | snake_case  |
| Functions  | snake_case  |
| Variables  | snake_case  |
| Constants  | UPPER_SNAKE_CASE |

# 2. Content Directory Structure
```
- res://
  - actors/
    - player/
      - player_character.gd
      - player_character.tscn
    - enemies/
      - enemy_ai.gd
      - enemy_ai.tscn
  - assets/
    - textures/
    - models/
    - sounds/
  - maps/
    - level1.tscn
    - level2.tscn
  - ui/
    - main_menu/
      - main_menu.gd
      - main_menu.tscn
    - hud/
      - hud.gd
      - hud.tscn
  - scripts/
    - utility/
      - math_functions.gd
    - managers/
      - game_manager.gd
  - addons/
```

# 3. GDScript

### 1. Indentation

Use tabs for indentation. Each level of indentation should be one tab.

### 2. Spacing

- Use spaces around operators. Example: `var a = b + c` not `var a=b+c`.
- Use a space after commas. Example: `func foo(a, b)` not `func foo(a,b)`.

### 3. Braces

- Opening braces should be on the same line as the statement which starts the block. Example: `if a > b:`
- Closing braces should be on a line of their own, except when followed by else: `} else {`.

### 4. Comments

- Use `#` for single line comments.
- Use `"""` for multi-line comments.

### 5. File Structure
Each GDScript file should generally follow this structure:
- **Imports**: At the top of the file, import any necessary modules or scripts.
- **Class Variables**: Declare any class-wide variables next.
- **Ready Function**: The `_ready()` function should come next, if used. This is where you initialize anything that needs to be set up at the start of the script.
- **Process Function**: The `_process(delta)` function should come next, if used. This is where you put code that needs to run every frame.
- **Other Functions**: Any other functions should come after. Try to group similar functions together for readability.

### 6. Grouping
Group related scripts together in the same directory. For example, all scripts related to player mechanics could go in a `player` directory.

# 4. Levels/Maps

# 5. Textures

## Texture Naming Conventions in Godot

1. **Diffuse/Albedo Textures**: `T_AssetName_D.tres` or `t_assetname_d.png`, etc.
   - Example: `T_Player_D.tres`, `t_player_d.png`.
2. **Normal Textures**: `T_AssetName_N.tres` or `t_assetname_n.png`, etc.
   - Example: `T_Player_N.tres`, `t_player_n.png`.
3. **Specular Textures**: `T_AssetName_S.tres` or `t_assetname_s.png`, etc.
   - Example: `T_Player_S.tres`, `t_player_s.png`.
4. **Emissive Textures**: `T_AssetName_E.tres` or `t_assetname_e.png`, etc.
   - Example: `T_Player_E.tres`, `t_player_e.png`.
5. **Roughness Textures**: `T_AssetName_R.tres` or `t_assetname_r.png`, etc.
   - Example: `T_Player_R.tres`, `t_player_r.png`.
6. **Metallic Textures**: `T_AssetName_M.tres` or `t_assetname_m.png`, etc.
   - Example: `T_Player_M.tres`, `t_player_m.png`.
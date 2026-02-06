ETER LANGUAGE
Official Specification — v0.2 (Alpha)
ETER is a declarative, universal, and human-readable language created to describe games (initially MOBA/FPS) in a simple, natural, and structured way, without requiring traditional programming knowledge.

It was designed for:

● Designers
● Beginning creators
● Generative AI
● Rapid prototyping
● Engines like Godot
LANGUAGE PHILOSOPHY
● ❌ Not procedural
● ❌ No if, for, while statements
● ❌ No variables or control logic
● ✅ Descriptive
● ✅ Declarative
● ✅ Deterministic
● ✅ Readable in Portuguese or English
● ✅ Describes what exists, not how to execute it

ETER describes the game.

The engine interprets it.

FILE EXTENSION .eter

Example:
my_game.eter

GENERAL FILE STRUCTURE
Start of code:
Name, GameName.
Block:
Property, Value.

General rules:
● Each instruction ends with a period (.).
● Blocks end with a colon (:).
● Spaces and indentation are free.
● Comments do not yet exist (v0.3).

META SECTION (GLOBAL)
Required
Start of code:
Name, Eter Moba Alpha.
Field Description
Name: Project/Game Name

BLOCK: Mode
Defines the main game type.

Mode:
Type, MOBA.

Supported Values:

● MOBA
● FPS (reserved)

● BLOCK: Map
Describes the overall map structure.

Map:
Type, MOBA.
Routes, 3.
Jungle, Active.
Allied Base, Active.
Enemy Base, Active.

BLOCK: Routes
Routes:
Top, Active.
Mid, Active.
Bottom, Active.

● BLOCK: Hero (MULTI)
Can be repeated multiple times.
Hero:
Name, Auron.
Class, Warrior.

Base Life, 600.
Base Mana, 300.
Base Damage, 60.
Speed, 340.

Common Fields:

● Name
● Class
● Base Life
● Base Mana
● Base Damage
● Speed

BLOCK: Class (MULTI)
Class:
Name, Warrior.
Bonus Life, 10%.
Bonus Defense, 5%.

BLOCK: Skill (MULTI)
Skill:
Name, Powerful Strike.
Type, Active.
Target, Enemy.
Range, Short.
Damage, 120.
Cost, 40.
Cooldown, 8s.

Range, Short.
Damage, 120.
Cost, 40.
Cooldown, 8s.

Types:
Active
Passive
Ultimate

BLOCK: Skill Kit
Relates heroes to skills.
Skill Kit:
Hero, Auron.
Skill 1, Powerful Strike.
Ultimate, War Fury.

BLOCK: Hero Progression
Hero Progression:
Max Level, 18.
Health Increase, 90.
Damage Increase, 4.

BLOCK: Monster (MULTI)
Jungle
Monster:
Name, Dragon.
Type, Jungle.
Health, 3500.
Bonus, Global.

Wandering Neutral
Monster:
Name, Wandering Colossus.
Type, Wandering Neutral.
Direction, Opposite Nexus.
Life, 1200.

BLOCK: Economy
Economy:
Money, Gold.
Premium Currency, Crystals.

BLOCK: Item (MULTI)
Item:
Name, Long Sword.
Type, Damage.
BonusDamage, 20.
Price, 350.

Cosmetic
Item:
Name, Fire Auron Skin.
Type, Cosmetic.
AffectsGameplay, No.

BLOCK: CommunityShop
CommunityShop:
Active.
AllowedContent, Cosmetics.
CreatorRevenue, 70%.

ACCEPTED VALUES
Type Example
Text Gold
Number 350
Boolean Active, Inactive
Percentage

l

70%

Time 8s, 90d
Accepted Aliases:

● Active, Yes, Allowed → true
● Inactive, No, Disabled → false

EXECUTION (PIPELINE)
file.eter
↓
eter build file.eter
↓
Godot project generated
↓ Godot interprets JSON

Generated files:

● eter_runtime.json
● heroes.json
● skills.json
● items.json
● monsters.json

WHAT DOES NOT EXIST (YET)
● Scripts
● Logic Conditional
● Real Multiplayer
● Physics
● Behavioral AI
● Visual Editor (ETER Studio – planned)

● ROADMAP
v0.3

● Comments
● Semantic Validation
● Basic Visual Editor

v0.4
● Declarative UI
● HUD / Client
● 3D Preview

● PROJECT GOAL ETER is not just a language.

It's a universal game design layer, readable by humans and AI, decoupled from the engine.

“If you can describe the game, you can create it.”

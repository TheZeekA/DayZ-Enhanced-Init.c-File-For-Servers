# 🎮 DayZ Enhanced Server Management System

A comprehensive server-side modification for DayZ that adds advanced player management, chat systems, and administrative tools to enhance your server experience.

## ✨ Features

### 🔧 **Server Configuration**
- **Automated Economy Initialization** - Seamless Hive integration with offline initialization
- **Date Reset System** - Configurable date management (default: September 20th reset)
- **Configurable Settings** - JSON-based configuration for easy customization
- **Auto-save Functionality** - Periodic data saving with configurable intervals

### 👥 **Player Management System**

#### **Player Registration & Tracking**
- Automatic player registration on first connection
- Notifies player about the current amount of other players on the server when they join
- Steam ID to player name mapping
- Connection history tracking
- Player statistics (kills, deaths, K/D ratio)

#### **Duplicate Name Prevention**
- Automatic detection of duplicate player names
- Configurable kick system for name conflicts
- "Survivor" name detection and warnings
- Grace period with multiple warnings before action

### 💬 **Advanced Chat System**

#### **Global & Local Chat**
- Toggle between global and local chat modes
- Per-player chat preferences
- Mute system integration
- Clean message formatting

#### **Chat Commands**
```
/chat local    - Switch to local chat only
/chat global   - Switch to global chat
/killfeed on   - Enable kill feed notifications (Is ON for ALL Players By Default)
/killfeed off  - Disable kill feed notifications
/stats         - Display personal statistics
```

### 🛡️ **Administrative Tools**

#### **Moderation System**
- **Permanent Muting** - Persistent mute system across sessions
- **Temporary Muting** - Time-based muting with auto-expiration
- **Admin/Mod Roles** - Hierarchical permission system
- **Teleportation Tools** - Coordinate-based teleportation for staff

#### **Admin Commands**
```
?mute perm [player]     - Permanently mute a player
?mute [minutes] [player] - Temporarily mute a player
?mute disable [player]   - Unmute a player
?tp coord [x] [y] [player] - Teleport player to coordinates
```

### 📊 **Kill Feed System**
- **Real-time Kill Notifications** - Display player kills with weapon information
- **Configurable Delays** - Customizable notification timing
- **Opt-in System** - Players can choose to receive kill notifications
- **Detailed Information** - Shows victim, killer, and weapon used
- **Statistics Tracking** - Automatic kill/death counting

### 📁 **Data Persistence**
- **JSON Configuration Files**:
  - `sysConfig.json` - Server settings and timers
  - `adminConfig.json` - Admin and moderation settings
  - `playersConfig.json` - Player data and statistics

### 🎯 **Spawn Enhancement**
- **Randomized Starting Equipment** - Varied spawn gear with random health values
- **Smart Item Distribution** - Bandages, chemlights, and food variety
- **Health Randomization** - Realistic wear on starting equipment

## 🚀 Installation

1. **Backup your existing `init.c` file**
2. Replace your current `init.c` with this enhanced version
3. Start your server to generate default configuration files
4. Customize settings in the generated JSON files as needed

## ⚙️ Configuration (These files will be in server rootfolder/config)

### System Configuration (`sysConfig.json`)
```json
{
  "killFeedNotifyMinutes": 0.2,
  "autoSaveMinutes": 4,
  "kickPlayersOnDuplicateName": 1,
  "serverRestartMinutes": 384,
  "debug_enabled": 0
}
```

### Admin Configuration (`adminConfig.json`)
```json
{
  "mutedPlayers": "steamid1 steamid2",
  "adminPlayers": "steamid1 steamid2", 
  "modPlayers": "steamid1 steamid2"
}
```

## 🔑 Key Benefits

- **🛠️ Reduced Administration Overhead** - Automated player management
- **🎪 Enhanced Player Experience** - Interactive chat and kill feed systems
- **🔒 Robust Moderation Tools** - Comprehensive muting and admin systems
- **📈 Player Retention** - Statistics tracking and personalized features
- **⚡ Performance Optimized** - Efficient data structures and minimal overhead
- **🔧 Highly Configurable** - JSON-based settings for easy customization

## 🎯 Perfect For

- **RP Servers** - Enhanced chat and player management
- **PvP Servers** - Kill feed and statistics tracking
- **Community Servers** - Comprehensive moderation tools
- **Large Servers** - Scalable player management system

## 📋 Requirements

- DayZ Server (Latest Version)
- Basic understanding of DayZ server administration
- Write access to server profile directory for JSON configuration files

## 🤝 Support

This system is designed to be robust and self-maintaining. All configurations are automatically generated with sensible defaults, and the system gracefully handles edge cases and errors.

---

*Transform your DayZ server into a professional, well-managed gaming environment with this comprehensive enhancement package.*
*Credit for idea and initial inic.c goes to https://github.com/joncantarino/DayZVanillaInit*

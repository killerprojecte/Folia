
<div align="center">
  <img src="logo.png" width="32%" height="32%"/>
  <p><b><font size="+3">DirtyKaiiju</font></b></p>
  <p>Fork of <a href="https://github.com/KaiijuMC/Kaiiju">Kaiiju</a> working to support more bukkit plugins.</p>

  [![License](https://img.shields.io/github/license/kugge/Kaiiju?style=for-the-badge&logo=github)](LICENSE)
  [![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/kugge/Kaiiju/build.yml?style=for-the-badge)](https://github.com/kugge/Kaiiju/actions)
  [![Discord](https://img.shields.io/discord/1059774886672859136?color=5865F2&label=discord&style=for-the-badge)](https://discord.gg/qagZRAepb7)

</div>

- **DirtyKaiiju** is a project to make **Kaijju** support more **Only Bukkit-API** plugins
- We will never support plugins that work based on NMS (Unsafe)
- All plugin compatible work needs to be based on whether the original Folia related API is available
- **This is the experimental branch of DirtyFolia**
## About Kaiiju ↓

## Features

### Primary
- **Xymb Linear Format**: Saves about 50% of disk space in OW/Nether and 95% in The End.
- **Auto update**: Automatic upstream updates.

### Notable
- **Optimize Hopper**: Enable/Disable Paper "Optimize Hopper" patch that break a lot of redstone farms.
- **Entity throttling & removal**: Tweak entity tick frequency & max entity per region.
- **Sand duplication**: Toggle sand duplication on Folia.

### Configuration

```yaml
verbose: false
region-format:
  debug: false
network:
  send-null-entity-packets: true
  alternate-keepalive: false
gameplay:
  server-mod-name: Kaiiju
  shared-random-for-players: true
world-settings:
  default:
    region-format:
      format: ANVIL
      linear:
        compression-level: 1
        crash-on-broken-symlink: true
    gameplay:
      shulker-box-drop-contents-when-destroyed: true
      fix-void-trading: true
      optimize-hoppers: true
      tick-when-empty: true
      break-redstone-on-top-of-trap-doors-early: true
config-version: 1
```
Documentation: [Kaiiju Wiki](https://github.com/KaiijuMC/Kaiiju/wiki/Configuration)

### Roadmap
- **Static view distance**: Reduce RAM usage / Region size with a "static" view distance.
- **Native world conversion**: Convert region file format at startup.
- **Stash deduplication**: Make giant dupe stashes possible and lagless.

## Building

```bash
./gradlew applyPatches # Apply Kaiiju patches
./gradlew createReobfPaperclipJar # Generate Paperclip executable jar
```

## License
Original patches are licensed under GPL-3.0.

# cnam3a_minecraft_server

Shared resource pack of the server. Every push to `main` builds `cnam3a_minecraft_server.zip` and publishes it as the latest release.

**Download link (always the newest build):**
`https://github.com/<owner>/cnam3a_minecraft_server/releases/latest/download/cnam3a_minecraft_server.zip`

## Adding your own content

1. Pick a namespace (your name or your project, lowercase, e.g. `steve` or `skybase`).
2. Put everything under `assets/<your_namespace>/`. Never edit another person's folder.
3. Open a pull request (or push, if you have access).

Sounds:

```
assets/<your_namespace>/sounds.json
assets/<your_namespace>/sounds/<file>.ogg
```

```json
{
  "my_sound": { "sounds": [ { "name": "<your_namespace>:my_sound" } ] }
}
```

Play it in game with `/playsound <your_namespace>:my_sound master @s`, or from ComputerCraft with `speaker.playSound("<your_namespace>:my_sound")`.

Rules for sounds: OGG Vorbis, **mono** (stereo files ignore distance), lowercase file names without spaces, keep each file small.

Textures and models work the same way (`assets/<your_namespace>/textures/...`). To change a vanilla or modded texture, use that mod's namespace, but tell the others first: two people editing the same file overwrite each other.

## Namespaces in use

| Namespace | Owner | Content |
| --- | --- | --- |
| `halcyon` | gwenaf | HALCYON jingles for `halcyon.lua` (`halcyon:jingle.<logo>`, `halcyon:idle.<logo>`) |

## After a new build

Each release lists its SHA-1. Copy it into the server's `server.properties` (`resource-pack-sha1=`) and restart the server, so players download the new version.

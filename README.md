<a name="top"></a>

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:8aadf4,50:c6a0f6,100:f5bde6&height=210&section=header&text=toasty&fontSize=72&fontColor=24273a&animation=fadeIn&fontAlignY=36&desc=probably%20debugging%20something%20right%20now&descAlignY=56&descSize=17&descColor=24273a"/>

<a href="https://github.com/woahtoasty">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=500&size=21&duration=3200&pause=1000&color=c6a0f6&center=true&vCenter=true&width=620&lines=writing+code+that+mostly+works;currently+poking+at+xbox+360+internals;big-endian+is+a+personality+trait+now;coffee+first%2C+questions+later" alt="typing" />
</a>

<br>

<a href="#about"><img src="https://img.shields.io/badge/about-24273a?style=for-the-badge&logo=aboutdotme&logoColor=8aadf4&labelColor=24273a" /></a>
<a href="#toastylink"><img src="https://img.shields.io/badge/toastylink-24273a?style=for-the-badge&logo=cplusplus&logoColor=c6a0f6&labelColor=24273a" /></a>
<a href="#activity"><img src="https://img.shields.io/badge/activity-24273a?style=for-the-badge&logo=githubactions&logoColor=f5bde6&labelColor=24273a" /></a>

</div>

<br>

<h3 id="about" align="center">✿ &nbsp;about&nbsp; ✿</h3>

I like taking things apart to see how they actually work, then putting them back together a little better than I found them. some days that's shipping something small and clean. other days it's three hours deep in a bug that turns out to be one byte in the wrong order. both count, honestly.

half the code I write is for future me, who somehow always ends up more annoyed at past me than the other way around. so I try to leave things in a state I won't hate opening again later.

<div align="center">

|  |  |
|---|---|
| 🧠 | rather understand *why* something works than just copy-paste a fix |
| 🚀 | small and shipped beats big and unfinished, every time |
| 📖 | I do read the docs first. mostly. |
| 🌱 | still learning plenty, not gonna pretend otherwise |

<br>

**stuff I reach for**

<img src="https://skillicons.dev/icons?i=cpp,cmake,git,github,visualstudio,windows,linux,apple&theme=dark" alt="tech" />

<br><br>

<img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight" alt="dev quote"/>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:24273a,30:8aadf4,50:c6a0f6,70:f5bde6,100:24273a&height=3"/>

</div>

<h3 id="toastylink" align="center">⋆ &nbsp;what I'm building&nbsp; ⋆</h3>

<div align="center">

## [ToastyLink](https://github.com/woahtoasty/ToastyLink)

<a href="https://github.com/woahtoasty/ToastyLink/releases/latest"><img src="https://img.shields.io/github/v/release/woahtoasty/ToastyLink?style=for-the-badge&color=c6a0f6&labelColor=24273a&logo=github&logoColor=c6a0f6" /></a>
<a href="https://github.com/woahtoasty/ToastyLink"><img src="https://img.shields.io/github/languages/top/woahtoasty/ToastyLink?style=for-the-badge&color=8aadf4&labelColor=24273a" /></a>
<a href="https://github.com/woahtoasty/ToastyLink/blob/main/LICENSE"><img src="https://img.shields.io/github/license/woahtoasty/ToastyLink?style=for-the-badge&color=8aadf4&labelColor=24273a" /></a>
<img src="https://img.shields.io/badge/windows%20%7C%20linux%20%7C%20macos-24273a?style=for-the-badge&labelColor=24273a&logo=cmake&logoColor=f5bde6" />

a from-scratch **C++17 trainer & debug toolkit** for XBDM — the protocol Xbox 360 consoles expose when running a softmodded dashboard. no third-party SDK, no bundled GUI: just the wire protocol implemented directly, with the workflow the RGH/JTAG community actually uses built on top of it.

|  |  |
|---|---|
| ⚡ | **typed, endian-correct memory access** — i8 through f64, handled explicitly for Xenon's big-endian PowerPC (the #1 source of silent bugs when a little-endian PC talks to it) |
| 🔗 | **pointer chains** — `base,off1,off2` resolves live, so an address survives game restarts instead of rotting on reboot |
| 🔍 | **progressive value scanning** — narrow an unknown health/ammo address down by playing between scans, Cheat Engine style |
| ❄️ | **a real freeze engine** — background thread, named entries, saved as small JSON cheat tables you can hand to someone else |
| 🧩 | **AOB pattern scanning** with wildcards, over a range or every mapped region |
| 📜 | **batch scripting + raw passthrough** — a whole trainer setup in one command, and correct framing for any XBDM command |

</div>

```console
toastylink> vscan new i32 0x82000000 0x200000 exact 100
414 candidate(s). Play/change the value, then run 'vscan next ...'.

toastylink> vscan next changed
6 candidate(s) remaining.

toastylink> vscan next decreased
1 candidate(s) remaining.  →  0x82045a10 = 73

toastylink> freeze add health i32 0x82045a10 100
toastylink> freeze start
freeze engine started (interval 200ms)
```

<div align="center">

no game-specific offsets are baked in anywhere — offsets go stale the moment a title updates, so it ships the primitives instead of a pile of addresses that would rot on day one.

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:24273a,30:f5bde6,50:c6a0f6,70:8aadf4,100:24273a&height=3"/>

</div>

<h3 id="activity" align="center">˚ &nbsp;activity&nbsp; ˚</h3>

<div align="center">

<img src="https://streak-stats.demolab.com/?user=woahtoasty&hide_border=true&theme=tokyonight&ring=c6a0f6&fire=f5bde6&currStreakLabel=8aadf4&background=24273a" alt="streak" width="58%"/>

<br><br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/woahtoasty/woahtoasty/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/woahtoasty/woahtoasty/output/github-contribution-grid-snake.svg" />
  <img alt="contribution snake" src="https://raw.githubusercontent.com/woahtoasty/woahtoasty/output/github-contribution-grid-snake.svg" width="95%"/>
</picture>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:24273a,30:8aadf4,50:c6a0f6,70:f5bde6,100:24273a&height=3"/>

thanks for scrolling this far ♡ &nbsp;poke around, star something if you feel like it, or [open an issue](https://github.com/woahtoasty/ToastyLink/issues) if you find something broken — you probably will, I move fast

<br>

<img src="https://komarev.com/ghpvc/?username=woahtoasty&label=profile+views&color=8aadf4&style=for-the-badge" alt="profile views"/>
<a href="#top"><img src="https://img.shields.io/badge/%E2%86%91%20back%20to%20top-24273a?style=for-the-badge&labelColor=24273a" /></a>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:f5bde6,50:c6a0f6,100:8aadf4&height=140&section=footer"/>

</div>

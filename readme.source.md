<!-- readme.source.md — Sahil Gwalvanshi GitHub Profile -->
<!-- Build: npx readme-aura build -->
<!-- Auto-rebuild: .github/workflows/readme-aura.yml -->

```aura width=862 height=220
export default function HeroBanner() {
  return (
    <div style={{
      width: 862,
      height: 220,
      background: "linear-gradient(135deg, #0a0a0f 0%, #0d1117 40%, #0a0e1a 100%)",
      display: "flex",
      flexDirection: "column",
      alignItems: "center",
      justifyContent: "center",
      position: "relative",
      overflow: "hidden",
      fontFamily: "Inter, sans-serif",
    }}>
      {/* Grid lines */}
      {[...Array(10)].map((_, i) => (
        <div key={i} style={{
          position: "absolute",
          top: 0, bottom: 0,
          left: `${i * 10}%`,
          width: 1,
          background: "rgba(99,102,241,0.06)",
        }} />
      ))}
      {[...Array(6)].map((_, i) => (
        <div key={i} style={{
          position: "absolute",
          left: 0, right: 0,
          top: `${i * 20}%`,
          height: 1,
          background: "rgba(99,102,241,0.06)",
        }} />
      ))}

      {/* Glow orbs */}
      <div style={{
        position: "absolute",
        top: -60,
        left: -60,
        width: 220,
        height: 220,
        borderRadius: "50%",
        background: "radial-gradient(circle, rgba(99,102,241,0.18) 0%, transparent 70%)",
      }} />
      <div style={{
        position: "absolute",
        bottom: -60,
        right: -40,
        width: 200,
        height: 200,
        borderRadius: "50%",
        background: "radial-gradient(circle, rgba(139,92,246,0.14) 0%, transparent 70%)",
      }} />
      <div style={{
        position: "absolute",
        top: 40,
        right: 120,
        width: 120,
        height: 120,
        borderRadius: "50%",
        background: "radial-gradient(circle, rgba(59,130,246,0.10) 0%, transparent 70%)",
      }} />

      {/* Floating dots */}
      {[
        {top:30,left:80,size:3,opacity:0.5},
        {top:60,left:200,size:2,opacity:0.4},
        {top:100,left:50,size:2,opacity:0.3},
        {top:20,left:700,size:3,opacity:0.5},
        {top:80,left:780,size:2,opacity:0.4},
        {top:160,left:650,size:2,opacity:0.3},
        {top:180,left:400,size:2,opacity:0.25},
        {top:40,left:500,size:2,opacity:0.3},
      ].map((d,i) => (
        <div key={i} style={{
          position: "absolute",
          top: d.top,
          left: d.left,
          width: d.size,
          height: d.size,
          borderRadius: "50%",
          background: `rgba(139,92,246,${d.opacity})`,
        }} />
      ))}

      {/* Greeting */}
      <div style={{
        display: "flex",
        alignItems: "center",
        gap: 10,
        marginBottom: 8,
      }}>
        <div style={{
          fontSize: 13,
          color: "rgba(139,92,246,0.9)",
          letterSpacing: "0.25em",
          textTransform: "uppercase",
          fontWeight: 500,
        }}>Hello World 👋</div>
      </div>

      {/* Main Name */}
      <div style={{
        display: "flex",
        alignItems: "center",
        gap: 14,
        marginBottom: 12,
      }}>
        <div style={{
          fontSize: 48,
          fontWeight: 800,
          color: "#ffffff",
          letterSpacing: "-0.02em",
          lineHeight: 1,
        }}>Sahil</div>
        <div style={{
          fontSize: 48,
          fontWeight: 800,
          background: "linear-gradient(90deg, #6366f1, #8b5cf6, #3b82f6)",
          color: "transparent",
          letterSpacing: "-0.02em",
          lineHeight: 1,
        }}>Gwalvanshi</div>
      </div>

      {/* Subtitle pills */}
      <div style={{ display: "flex", gap: 10, alignItems: "center" }}>
        {["💻 Full Stack Developer", "🇮🇳 India", "🎓 CS Student"].map((tag, i) => (
          <div key={i} style={{
            padding: "4px 14px",
            borderRadius: 999,
            border: "1px solid rgba(99,102,241,0.35)",
            background: "rgba(99,102,241,0.08)",
            fontSize: 12,
            color: "rgba(200,200,255,0.85)",
            fontWeight: 500,
          }}>{tag}</div>
        ))}
      </div>
    </div>
  );
}
```

```aura width=862 height=200
export default function AboutMe() {
  return (
    <div style={{
      width: 862,
      height: 200,
      background: "#0d1117",
      display: "flex",
      padding: "0 24px",
      gap: 24,
      fontFamily: "Inter, sans-serif",
      alignItems: "stretch",
    }}>
      {/* Left — main about card */}
      <div style={{
        flex: 1,
        background: "rgba(99,102,241,0.05)",
        border: "1px solid rgba(99,102,241,0.18)",
        borderRadius: 16,
        padding: "20px 24px",
        display: "flex",
        flexDirection: "column",
        justifyContent: "space-between",
      }}>
        <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 14 }}>
          <div style={{
            width: 6,
            height: 6,
            borderRadius: "50%",
            background: "#6366f1",
          }} />
          <div style={{ fontSize: 11, color: "#6366f1", letterSpacing: "0.18em", textTransform: "uppercase", fontWeight: 600 }}>
            About Me
          </div>
        </div>

        <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
          {[
            { icon: "🎓", text: "CS student with strong interest in tech & problem-solving" },
            { icon: "⚡", text: "Currently learning Data Structures, Algorithms & core programming" },
            { icon: "🎯", text: "Goal: become a skilled software engineer & build real-world projects" },
            { icon: "🔥", text: "Focused on consistency, continuous learning, and personal growth" },
          ].map((item, i) => (
            <div key={i} style={{ display: "flex", alignItems: "flex-start", gap: 8 }}>
              <div style={{ fontSize: 13, lineHeight: "18px", flexShrink: 0 }}>{item.icon}</div>
              <div style={{ fontSize: 12, color: "rgba(200,210,255,0.75)", lineHeight: "18px" }}>{item.text}</div>
            </div>
          ))}
        </div>
      </div>

      {/* Right — quick stats */}
      <div style={{
        width: 220,
        display: "flex",
        flexDirection: "column",
        gap: 10,
      }}>
        {[
          { label: "Focus", value: "Full Stack", color: "#6366f1" },
          { label: "Learning", value: "DSA + Algorithms", color: "#8b5cf6" },
          { label: "Open to", value: "Collaborations", color: "#3b82f6" },
          { label: "Status", value: "Building 🚀", color: "#06b6d4" },
        ].map((s, i) => (
          <div key={i} style={{
            flex: 1,
            background: "rgba(99,102,241,0.05)",
            border: "1px solid rgba(99,102,241,0.15)",
            borderRadius: 10,
            padding: "0 14px",
            display: "flex",
            alignItems: "center",
            justifyContent: "space-between",
          }}>
            <div style={{ fontSize: 11, color: "rgba(150,160,200,0.6)", fontWeight: 500 }}>{s.label}</div>
            <div style={{ fontSize: 11, color: s.color, fontWeight: 600 }}>{s.value}</div>
          </div>
        ))}
      </div>
    </div>
  );
}
```

```aura width=862 height=240
export default function TechStack() {
  const skills = [
    { name: "JavaScript", color: "#f7df1e", bg: "rgba(247,223,30,0.1)", border: "rgba(247,223,30,0.3)" },
    { name: "TypeScript", color: "#3178c6", bg: "rgba(49,120,198,0.1)", border: "rgba(49,120,198,0.3)" },
    { name: "React", color: "#61dafb", bg: "rgba(97,218,251,0.1)", border: "rgba(97,218,251,0.3)" },
    { name: "Node.js", color: "#68a063", bg: "rgba(104,160,99,0.1)", border: "rgba(104,160,99,0.3)" },
    { name: "Python", color: "#3572A5", bg: "rgba(53,114,165,0.1)", border: "rgba(53,114,165,0.3)" },
    { name: "HTML5", color: "#e34c26", bg: "rgba(227,76,38,0.1)", border: "rgba(227,76,38,0.3)" },
    { name: "CSS3", color: "#264de4", bg: "rgba(38,77,228,0.1)", border: "rgba(38,77,228,0.3)" },
    { name: "C++", color: "#00599c", bg: "rgba(0,89,156,0.1)", border: "rgba(0,89,156,0.3)" },
    { name: "Git", color: "#f05032", bg: "rgba(240,80,50,0.1)", border: "rgba(240,80,50,0.3)" },
    { name: "GitHub", color: "#ffffff", bg: "rgba(255,255,255,0.06)", border: "rgba(255,255,255,0.2)" },
    { name: "VS Code", color: "#007acc", bg: "rgba(0,122,204,0.1)", border: "rgba(0,122,204,0.3)" },
    { name: "Tailwind", color: "#38bdf8", bg: "rgba(56,189,248,0.1)", border: "rgba(56,189,248,0.3)" },
    { name: "MongoDB", color: "#47a248", bg: "rgba(71,162,72,0.1)", border: "rgba(71,162,72,0.3)" },
    { name: "Firebase", color: "#ffca28", bg: "rgba(255,202,40,0.1)", border: "rgba(255,202,40,0.3)" },
    { name: "Docker", color: "#2496ed", bg: "rgba(36,150,237,0.1)", border: "rgba(36,150,237,0.3)" },
  ];

  return (
    <div style={{
      width: 862,
      height: 240,
      background: "#0d1117",
      fontFamily: "Inter, sans-serif",
      padding: "0 24px",
      display: "flex",
      flexDirection: "column",
    }}>
      {/* Header */}
      <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 18 }}>
        <div style={{ width: 6, height: 6, borderRadius: "50%", background: "#8b5cf6" }} />
        <div style={{ fontSize: 11, color: "#8b5cf6", letterSpacing: "0.18em", textTransform: "uppercase", fontWeight: 600 }}>
          Tech Stack
        </div>
        <div style={{ flex: 1, height: 1, background: "rgba(99,102,241,0.15)" }} />
      </div>

      {/* Pills row 1 */}
      <div style={{ display: "flex", gap: 8, flexWrap: "wrap", marginBottom: 8 }}>
        {skills.slice(0, 8).map((s, i) => (
          <div key={i} style={{
            padding: "6px 14px",
            borderRadius: 999,
            background: s.bg,
            border: `1px solid ${s.border}`,
            fontSize: 12,
            color: s.color,
            fontWeight: 600,
            letterSpacing: "0.02em",
          }}>
            {s.name}
          </div>
        ))}
      </div>

      {/* Pills row 2 */}
      <div style={{ display: "flex", gap: 8, flexWrap: "wrap" }}>
        {skills.slice(8).map((s, i) => (
          <div key={i} style={{
            padding: "6px 14px",
            borderRadius: 999,
            background: s.bg,
            border: `1px solid ${s.border}`,
            fontSize: 12,
            color: s.color,
            fontWeight: 600,
            letterSpacing: "0.02em",
          }}>
            {s.name}
          </div>
        ))}
      </div>

      {/* Bottom label */}
      <div style={{ marginTop: "auto", paddingTop: 12, display: "flex", alignItems: "center", gap: 6 }}>
        <div style={{ fontSize: 11, color: "rgba(150,160,200,0.4)" }}>Always learning. Always building.</div>
      </div>
    </div>
  );
}
```

```aura width=862 height=130
export default function SocialConnect() {
  const socials = [
    {
      name: "LinkedIn",
      handle: "sahil-gwalvanshi",
      url: "https://www.linkedin.com/in/sahil-gwalvanshi-66544136a/",
      color: "#0a66c2",
      bg: "rgba(10,102,194,0.08)",
      border: "rgba(10,102,194,0.3)",
      icon: "in",
    },
    {
      name: "Instagram",
      handle: "@itssahilgwalvanshi",
      url: "https://www.instagram.com/itssahilgwalvanshi",
      color: "#e1306c",
      bg: "rgba(225,48,108,0.08)",
      border: "rgba(225,48,108,0.3)",
      icon: "ig",
    },
    {
      name: "Twitter / X",
      handle: "@SahilGwalvanshi",
      url: "https://x.com/SahilGwalvanshi",
      color: "#ffffff",
      bg: "rgba(255,255,255,0.05)",
      border: "rgba(255,255,255,0.18)",
      icon: "x",
    },
    {
      name: "Discord",
      handle: "sahilgwalvanshi",
      url: "https://discord.com/channels/sahilgwalvanshi",
      color: "#5865f2",
      bg: "rgba(88,101,242,0.08)",
      border: "rgba(88,101,242,0.3)",
      icon: "dc",
    },
    {
      name: "GitHub",
      handle: "sahilgwalvansh-gif",
      url: "https://github.com/sahilgwalvansh-gif",
      color: "#ffffff",
      bg: "rgba(255,255,255,0.05)",
      border: "rgba(255,255,255,0.18)",
      icon: "gh",
    },
  ];

  return (
    <div style={{
      width: 862,
      height: 130,
      background: "#0d1117",
      fontFamily: "Inter, sans-serif",
      padding: "0 24px",
      display: "flex",
      flexDirection: "column",
    }}>
      <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 16 }}>
        <div style={{ width: 6, height: 6, borderRadius: "50%", background: "#3b82f6" }} />
        <div style={{ fontSize: 11, color: "#3b82f6", letterSpacing: "0.18em", textTransform: "uppercase", fontWeight: 600 }}>
          Connect With Me
        </div>
        <div style={{ flex: 1, height: 1, background: "rgba(99,102,241,0.15)" }} />
      </div>

      <div style={{ display: "flex", gap: 10 }}>
        {socials.map((s, i) => (
          <div key={i} style={{
            flex: 1,
            background: s.bg,
            border: `1px solid ${s.border}`,
            borderRadius: 12,
            padding: "10px 14px",
            display: "flex",
            flexDirection: "column",
            gap: 4,
          }}>
            <div style={{ fontSize: 10, color: s.color, fontWeight: 700, letterSpacing: "0.05em" }}>{s.name}</div>
            <div style={{ fontSize: 10, color: "rgba(180,190,220,0.55)", fontWeight: 500 }}>{s.handle}</div>
          </div>
        ))}
      </div>
    </div>
  );
}
```

```aura width=862 height=210
export default function GitHubStats() {
  return (
    <div style={{
      width: 862,
      height: 210,
      background: "#0d1117",
      fontFamily: "Inter, sans-serif",
      padding: "0 24px",
      display: "flex",
      flexDirection: "column",
    }}>
      {/* Header */}
      <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 16 }}>
        <div style={{ width: 6, height: 6, borderRadius: "50%", background: "#06b6d4" }} />
        <div style={{ fontSize: 11, color: "#06b6d4", letterSpacing: "0.18em", textTransform: "uppercase", fontWeight: 600 }}>
          GitHub Stats
        </div>
        <div style={{ flex: 1, height: 1, background: "rgba(99,102,241,0.15)" }} />
      </div>

      {/* Stats row */}
      <div style={{ display: "flex", gap: 12, flex: 1 }}>
        {/* Main stats block */}
        <div style={{
          flex: 1,
          background: "rgba(6,182,212,0.05)",
          border: "1px solid rgba(6,182,212,0.18)",
          borderRadius: 14,
          padding: "16px 20px",
          display: "flex",
          flexDirection: "column",
          justifyContent: "space-between",
        }}>
          <div style={{ fontSize: 11, color: "rgba(150,160,200,0.6)", marginBottom: 12, fontWeight: 600 }}>OVERALL STATS</div>
          <div style={{ display: "flex", gap: 20 }}>
            {[
              { label: "Total Contributions", value: "101+" },
              { label: "Commits (2025)", value: "52" },
              { label: "Repositories", value: "6+" },
            ].map((stat, i) => (
              <div key={i} style={{ display: "flex", flexDirection: "column", gap: 4 }}>
                <div style={{ fontSize: 26, fontWeight: 800, color: "#06b6d4" }}>{stat.value}</div>
                <div style={{ fontSize: 10, color: "rgba(150,160,200,0.55)", fontWeight: 500 }}>{stat.label}</div>
              </div>
            ))}
          </div>
          {/* Progress bar */}
          <div style={{ marginTop: 14 }}>
            <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 6 }}>
              <div style={{ fontSize: 10, color: "rgba(150,160,200,0.5)" }}>Contribution streak progress</div>
              <div style={{ fontSize: 10, color: "#06b6d4" }}>8 days longest</div>
            </div>
            <div style={{ height: 4, background: "rgba(6,182,212,0.12)", borderRadius: 999 }}>
              <div style={{ height: 4, width: "65%", background: "linear-gradient(90deg, #06b6d4, #3b82f6)", borderRadius: 999 }} />
            </div>
          </div>
        </div>

        {/* Languages */}
        <div style={{
          width: 220,
          background: "rgba(139,92,246,0.05)",
          border: "1px solid rgba(139,92,246,0.18)",
          borderRadius: 14,
          padding: "16px 20px",
          display: "flex",
          flexDirection: "column",
          justifyContent: "space-between",
        }}>
          <div style={{ fontSize: 11, color: "rgba(150,160,200,0.6)", marginBottom: 10, fontWeight: 600 }}>TOP LANGUAGES</div>
          {[
            { lang: "JavaScript", pct: 56, color: "#f7df1e" },
            { lang: "HTML", pct: 30, color: "#e34c26" },
            { lang: "CSS", pct: 14, color: "#264de4" },
          ].map((l, i) => (
            <div key={i} style={{ marginBottom: 8 }}>
              <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 4 }}>
                <div style={{ fontSize: 11, color: l.color, fontWeight: 600 }}>{l.lang}</div>
                <div style={{ fontSize: 10, color: "rgba(150,160,200,0.5)" }}>{l.pct}%</div>
              </div>
              <div style={{ height: 3, background: "rgba(255,255,255,0.06)", borderRadius: 999 }}>
                <div style={{ height: 3, width: `${l.pct}%`, background: l.color, borderRadius: 999, opacity: 0.8 }} />
              </div>
            </div>
          ))}
        </div>

        {/* Streak / activity */}
        <div style={{
          width: 160,
          background: "rgba(99,102,241,0.05)",
          border: "1px solid rgba(99,102,241,0.18)",
          borderRadius: 14,
          padding: "16px 20px",
          display: "flex",
          flexDirection: "column",
          alignItems: "center",
          justifyContent: "center",
          gap: 8,
        }}>
          <div style={{ fontSize: 11, color: "rgba(150,160,200,0.6)", fontWeight: 600, textAlign: "center" }}>CURRENT STREAK</div>
          <div style={{
            width: 70,
            height: 70,
            borderRadius: "50%",
            border: "2px solid rgba(99,102,241,0.4)",
            display: "flex",
            alignItems: "center",
            justifyContent: "center",
            flexDirection: "column",
          }}>
            <div style={{ fontSize: 24, fontWeight: 800, color: "#6366f1" }}>0</div>
            <div style={{ fontSize: 9, color: "rgba(150,160,200,0.5)" }}>days</div>
          </div>
          <div style={{ fontSize: 10, color: "rgba(150,160,200,0.45)", textAlign: "center" }}>
            Last active May 27
          </div>
        </div>
      </div>
    </div>
  );
}
```

```aura width=862 height=160
export default function PinnedRepos() {
  const repos = [
    {
      name: "Aura-Project",
      desc: "Full-stack project showcase",
      lang: "JavaScript",
      langColor: "#f7df1e",
      stars: 1,
    },
    {
      name: "EduPath-Advisor",
      desc: "Education guidance platform",
      lang: "JavaScript",
      langColor: "#f7df1e",
      stars: 0,
    },
    {
      name: "sahilgwalvansh-gif",
      desc: "✨ Profile README · This file",
      lang: "Markdown",
      langColor: "#083fa1",
      stars: 0,
    },
    {
      name: "Assignment-1",
      desc: "CSS assignment project",
      lang: "CSS",
      langColor: "#264de4",
      stars: 0,
    },
  ];

  return (
    <div style={{
      width: 862,
      height: 160,
      background: "#0d1117",
      fontFamily: "Inter, sans-serif",
      padding: "0 24px",
      display: "flex",
      flexDirection: "column",
    }}>
      <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 14 }}>
        <div style={{ width: 6, height: 6, borderRadius: "50%", background: "#f59e0b" }} />
        <div style={{ fontSize: 11, color: "#f59e0b", letterSpacing: "0.18em", textTransform: "uppercase", fontWeight: 600 }}>
          Pinned Repos
        </div>
        <div style={{ flex: 1, height: 1, background: "rgba(99,102,241,0.15)" }} />
      </div>

      <div style={{ display: "flex", gap: 10, flex: 1 }}>
        {repos.map((r, i) => (
          <div key={i} style={{
            flex: 1,
            background: "rgba(99,102,241,0.04)",
            border: "1px solid rgba(99,102,241,0.14)",
            borderRadius: 12,
            padding: "12px 14px",
            display: "flex",
            flexDirection: "column",
            justifyContent: "space-between",
          }}>
            <div>
              <div style={{ fontSize: 12, color: "#6366f1", fontWeight: 700, marginBottom: 4 }}>{r.name}</div>
              <div style={{ fontSize: 10, color: "rgba(180,190,220,0.55)", lineHeight: "14px" }}>{r.desc}</div>
            </div>
            <div style={{ display: "flex", alignItems: "center", gap: 8 }}>
              <div style={{
                width: 8, height: 8, borderRadius: "50%",
                background: r.langColor, flexShrink: 0,
              }} />
              <div style={{ fontSize: 10, color: "rgba(150,160,200,0.55)" }}>{r.lang}</div>
              <div style={{ marginLeft: "auto", fontSize: 10, color: "rgba(150,160,200,0.4)" }}>⭐ {r.stars}</div>
            </div>
          </div>
        ))}
      </div>
    </div>
  );
}
```

```aura width=862 height=100
export default function Footer() {
  const quote = "Code is like humor. When you have to explain it, it's bad.";
  const author = "— Cory House";

  return (
    <div style={{
      width: 862,
      height: 100,
      background: "linear-gradient(135deg, #0a0a0f 0%, #0d1117 60%, #0a0e1a 100%)",
      fontFamily: "Inter, sans-serif",
      display: "flex",
      alignItems: "center",
      justifyContent: "space-between",
      padding: "0 32px",
      position: "relative",
      overflow: "hidden",
    }}>
      {/* Grid lines */}
      {[...Array(8)].map((_, i) => (
        <div key={i} style={{
          position: "absolute",
          top: 0, bottom: 0,
          left: `${i * 14}%`,
          width: 1,
          background: "rgba(99,102,241,0.05)",
        }} />
      ))}

      {/* Quote */}
      <div style={{ display: "flex", flexDirection: "column", gap: 4, maxWidth: 500 }}>
        <div style={{ fontSize: 13, color: "rgba(200,200,255,0.65)", fontStyle: "italic", lineHeight: "18px" }}>
          "{quote}"
        </div>
        <div style={{ fontSize: 11, color: "rgba(99,102,241,0.7)", fontWeight: 600 }}>{author}</div>
      </div>

      {/* Right — open to collab badge */}
      <div style={{ display: "flex", flexDirection: "column", alignItems: "flex-end", gap: 8 }}>
        <div style={{
          padding: "6px 16px",
          borderRadius: 999,
          background: "rgba(99,102,241,0.12)",
          border: "1px solid rgba(99,102,241,0.35)",
          fontSize: 11,
          color: "#818cf8",
          fontWeight: 600,
          display: "flex",
          alignItems: "center",
          gap: 6,
        }}>
          <div style={{ width: 6, height: 6, borderRadius: "50%", background: "#4ade80" }} />
          Open to collaborations
        </div>
        <div style={{ fontSize: 10, color: "rgba(150,160,200,0.3)" }}>
          powered by readme-aura
        </div>
      </div>
    </div>
  );
}
```

---

<!-- Live GitHub Stats — these use the readme-stats service and render as live images -->

<div align="center">

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=sahilgwalvansh-gif&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=6366f1&icon_color=8b5cf6&text_color=c9d1d9&ring_color=6366f1)](https://github.com/sahilgwalvansh-gif)
&nbsp;&nbsp;
[![GitHub Streak](https://streak-stats.demolab.com/?user=sahilgwalvansh-gif&theme=tokyonight&hide_border=true&background=0d1117&ring=6366f1&fire=8b5cf6&currStreakLabel=c9d1d9&sideLabels=6366f1)](https://github.com/sahilgwalvansh-gif)

</div>

---

<!-- Contribution Snake — add this after enabling GitHub Actions for it -->
<!-- Uncomment once you have the snake workflow set up: -->
<!-- <div align="center">
  <img src="https://raw.githubusercontent.com/sahilgwalvansh-gif/sahilgwalvansh-gif/output/github-contribution-grid-snake-dark.svg" alt="snake animation" />
</div> -->
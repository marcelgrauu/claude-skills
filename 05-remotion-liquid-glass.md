# Remotion Liquid Glass — Marcel Grau Style

## Quan usar
Quan Marcel demani crear motion graphics, reels, slides o qualsevol composició Remotion en el seu estil personal: Apple Liquid Glass + tipografia Inter/Garamond + degradats + glow.

---

## Sistema de disseny complet

### Paleta
```tsx
const YELLOW = "#FFFF00";
const BLACK = "#000000";
const WHITE = "#FFFFFF";
```

### Fons
```tsx
// bg-blue.jpg ha d'estar a /public del projecte Remotion
<Img src={staticFile("bg-blue.jpg")} style={{ position:"absolute", inset:0, width:"100%", height:"100%", objectFit:"cover" }} />
<div style={{ position:"absolute", inset:0, background:"rgba(0,0,20,0.45)" }} />
```

### Glass Card
```tsx
<div style={{
  position: "absolute",
  top: "50%", left: 60, right: 60,
  transform: `translateY(-50%) scale(${cardScale})`,
  opacity: cardOpacity,
  background: "rgba(255,255,255,0.07)",
  backdropFilter: "blur(24px)",
  WebkitBackdropFilter: "blur(24px)",
  borderRadius: 32,
  border: "1px solid rgba(255,255,255,0.14)",
  boxShadow: "inset 0 1px 0 rgba(255,255,255,0.18), inset 0 -1px 0 rgba(255,255,255,0.04), 0 8px 48px rgba(0,0,0,0.5)",
  padding: "64px 64px 72px",
  overflow: "hidden",
}}>
  {/* Specular highlight top */}
  <div style={{ position:"absolute", top:0, left:0, right:0, height:1, background:"linear-gradient(90deg, transparent, rgba(255,255,255,0.45) 50%, transparent)" }} />
  {/* contingut aquí */}
</div>
```

---

## Receptes de text

### Títol principal — Inter ExtraBold, blanc, glow
```tsx
<div style={{
  fontFamily: "'Inter', sans-serif",
  fontWeight: 800,
  color: "#FFFFFF",
  fontSize: 140,
  lineHeight: 0.85,
  letterSpacing: -11,
  whiteSpace: "nowrap",
  textShadow: "0 0 20px rgba(255,255,255,0.4), 0 0 40px rgba(255,255,255,0.12)",
}}>
  VIRAL HOOK
</div>
```

### Títol accent — Inter Light, degradat blanc→groc, glow groc
```tsx
<div style={{
  fontFamily: "'Inter', sans-serif",
  fontWeight: 300,
  fontSize: 140,
  lineHeight: 0.85,
  letterSpacing: -11,
  whiteSpace: "nowrap",
  background: "linear-gradient(180deg, #FFFFFF 0%, #FFFF00 80%)",
  WebkitBackgroundClip: "text",
  WebkitTextFillColor: "transparent",
  backgroundClip: "text",
  filter: "drop-shadow(0 0 12px rgba(255,255,0,0.5)) drop-shadow(0 0 30px rgba(255,255,0,0.18))",
}}>
  CREATOR
</div>
```

### Número índex — Helvetica Thin, discret
```tsx
<div style={{
  fontFamily: "'Helvetica Neue', Helvetica, Arial, sans-serif",
  fontWeight: 100,
  color: "#FFFFFF",
  fontSize: 32,
  letterSpacing: 5,
  opacity: 0.45,
  textShadow: "0 0 15px rgba(255,255,255,0.3)",
}}>
  01 / 05
</div>
```

### Descripció context — Helvetica Thin, blanc suau
```tsx
<div style={{
  fontFamily: "'Helvetica Neue', Helvetica, Arial, sans-serif",
  fontWeight: 100,
  color: "#FFFFFF",
  fontSize: 40,
  lineHeight: 1.35,
  letterSpacing: -1,
  opacity: 0.6,
  textShadow: "0 0 20px rgba(255,255,255,0.4), 0 0 40px rgba(255,255,255,0.12)",
}}>
  10 hooks. 5 seconds.
</div>
```

### Descripció punch — EB Garamond, degradat groc, glow
```tsx
<div style={{
  fontFamily: "'EB Garamond', 'Cormorant Garamond', Georgia, serif",
  fontWeight: 800,
  fontSize: 46,
  lineHeight: 1.2,
  letterSpacing: -2,
  background: "linear-gradient(180deg, #FFFFFF 0%, #FFFF00 80%)",
  WebkitBackgroundClip: "text",
  WebkitTextFillColor: "transparent",
  backgroundClip: "text",
  filter: "drop-shadow(0 0 12px rgba(255,255,0,0.5)) drop-shadow(0 0 30px rgba(255,255,0,0.18))",
}}>
  Stop the scroll.
</div>
```

### Watermark
```tsx
<div style={{
  fontFamily: "'Helvetica Neue', Helvetica, Arial, sans-serif",
  fontWeight: 100,
  color: "#FFFFFF",
  position: "absolute",
  bottom: 72, right: 72,
  fontSize: 22,
  letterSpacing: 1,
  opacity: 0.3,
  textShadow: "0 0 15px rgba(255,255,255,0.4)",
}}>
  marcelgrau.
</div>
```

---

## Animacions estàndard

```tsx
const frame = useCurrentFrame();

// Card entrada (spring)
const cardScale = spring({ frame, fps: 30, config: { damping: 18, stiffness: 220 } });
const cardOpacity = interpolate(frame, [0, 20], [0, 1], { extrapolateRight: "clamp" });

// Número fade in
const numOpacity = interpolate(frame, [0, 15], [0, 1], { extrapolateRight: "clamp" });

// Línia 1 títol (slide up)
const keyY = interpolate(frame, [8, 28], [50, 0], { extrapolateRight: "clamp", easing: Easing.out(Easing.cubic) });
const keyOpacity = interpolate(frame, [8, 28], [0, 1], { extrapolateRight: "clamp" });

// Línia 2 títol (slide up, delayed)
const supportY = interpolate(frame, [18, 36], [40, 0], { extrapolateRight: "clamp", easing: Easing.out(Easing.cubic) });
const supportOpacity = interpolate(frame, [18, 36], [0, 1], { extrapolateRight: "clamp" });

// Descripció (fade + slide up)
const descOpacity = interpolate(frame, [40, 62], [0, 1], { extrapolateRight: "clamp" });
const descY = interpolate(frame, [40, 62], [24, 0], { extrapolateRight: "clamp" });
```

---

## Setup (index.css)
```css
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=EB+Garamond:ital,wght@0,400;0,700;0,800;1,400;1,700&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,700;1,300;1,400&family=Inter:wght@300;700;800&display=swap');
```

## Imports Remotion
```tsx
import { AbsoluteFill, useCurrentFrame, interpolate, spring, Easing, Img, staticFile } from "remotion";
```

## Format composició
- 1080 × 1920 px, 30fps, 9:16 (Instagram/TikTok)
- Durada typical skill slide: 120 frames (4s)

---

## Notes
- Si el text es talla al card: reduir fontSize a 110-120
- El degradat `linear-gradient(180deg, ...)` va de blanc (dalt) a groc (baix) — es pot canviar per `90deg` per horitzontal
- `textShadow` NO funciona amb `WebkitTextFillColor: "transparent"` — usar sempre `filter: drop-shadow` per al text amb degradat
- `bg-blue.jpg` ha d'estar a la carpeta `/public` del projecte Remotion

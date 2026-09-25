---
name: forensic-image-to-json
description: >-
  Forensic-grade visual reverse-engineering system that transforms any single image,
  social media post, or multi-slide carousel (LinkedIn, Instagram, Facebook, X) into
  an exhaustive, ultra-detailed JSON prompt specification and a replica-ready master
  text prompt for Flux.1, Midjourney v6, Ideogram 2, and DALL-E 3.
---

# Forensic Image-to-JSON & Master Replica Prompt Skill

## Overview
This skill is a **Forensic Visual Reverse-Engineering Engine**. When given an image, multiple images, or a social media URL (LinkedIn carousel, Instagram post/carousel, Facebook graphic, X/Twitter thread), it performs a comprehensive pixel-level deconstruction.

It generates two synchronized outputs:
1. **`replica_json_spec`**: An ultra-exhaustive, machine-readable JSON object capturing all photographic physics (camera, lens, f-stop, shutter, ISO, lighting setup, Kelvin temp, shadows), graphic design (3D/2D elements, materials, opacity gradients, UI overlays), brand color tokens (exact hex codes), and 100% verbatim text transcription (zero spelling mistakes, exact casing, font anatomy, and spatial layout).
2. **`master_image_prompt`**: A production-ready, dense descriptive text prompt formatted for state-of-the-art AI image generators (FLUX.1 Pro/Schnell, Midjourney v6.1, Ideogram 2.0, DALL-E 3, Google Imagen 3) with exact text strings enclosed in quotation marks and camera/lighting parameters clearly stated.

---

## Supported Input Modes
1. **Direct Image Upload**: Single visual asset (photo, poster, product mockup, 3D render, infographic).
2. **Multiple Image Uploads**: Sequence of slides, carousel cards, or image variants.
3. **Social Media URLs**:
   - LinkedIn Post / Document Carousel (PDF slides or multi-image)
   - Instagram Single Post or Multi-slide Carousel
   - Facebook Post / Infographic / Ad Creative
   - X (Twitter) Post / Thread with images
   - Direct Web Image URLs

*When a URL is supplied, the agent fetches or inspects the visual media (using browser inspection or scraping tools), extracts each slide in sequence, and applies the carousel workflow.*

---

## Multi-Slide & Carousel Workflow
If the input contains multiple slides or a carousel:
1. **Extract Global Brand Style Guide (`global_carousel_tokens`)**:
   - Establish unifying brand elements: dominant color palette, typography hierarchy, logo placement, background textures, visual tone, and template padding.
2. **Slide-by-Slide Extraction (`slides[]`)**:
   - Process each slide (`slide_1`, `slide_2`, ... `slide_N`) individually.
   - For every slide, produce both the full JSON specification and the individual master replica prompt.
   - Maintain visual continuity while detailing slide-specific text, diagrams, focal 3D icons, and pagination counters (e.g., "01 / 07", "Swipe →").

---

## Forensic Deconstruction Checklist

### 1. Canvas & Compositional Geometry
- **Aspect Ratio & Canvas**: Exact ratio (`1:1`, `4:5`, `9:16`, `16:9`, `3:2`), pixel dimensions, orientation.
- **Compositional Grid**: Rule of thirds, golden spiral, symmetrical center, diagonal split, isometric grid, card layout.
- **Negative Space & Breathing Room**: Estimated percentage of uncrowded negative space.
- **Z-Index Layer Hierarchy**:
  - `Layer 0 (Background)`: Color, gradient angle, texture, blur backdrop.
  - `Layer 1 (Ambient / Environment)`: Grids, particles, bokeh, glowing orbs, decorative lines.
  - `Layer 2 (Primary Midground Subject)`: Main product, person, 3D object, or hero visual.
  - `Layer 3 (Secondary Floating Elements)`: 3D icons, badges, stickers, arrows, status pills.
  - `Layer 4 (Typography & UI Overlays)`: Headings, body text, buttons, pagination dots, watermarks.
  - `Layer 5 (Lens Effects & Atmospheric Post-Processing)`: Grain, dust, vignettes, bloom, lens flare, chromatic aberration.

### 2. Photographic & Cinematographic Physics
- **Camera Body & Sensor**: Full-frame 35mm, Medium Format (Hasselblad H6D-100c / Phase One), Cinema Camera (Arri Alexa 65), or Studio Macro.
- **Lens Optics & Focal Length**: Ultra-wide (14–20mm), Wide (24–35mm), Standard/Human eye (50mm), Portrait Telephoto (85–105mm), Super-telephoto (200mm+), or Macro (100mm 1:1 reproduction).
- **Aperture & Depth of Field (DoF)**:
  - Aperture f-stop (`f/1.2`, `f/1.8`, `f/2.8`, `f/5.6`, `f/11`).
  - DoF falloff: Ultra-shallow with creamy circular/anamorphic bokeh, or deep focus with edge-to-edge sharpness.
- **Shutter & Motion Dynamics**: Fast freeze (`1/2000s`), standard (`1/125s`), or motion blur / light streaks (`1/15s` or long exposure).
- **Sensor ISO & Texture**: Clean ISO 50/100, subtle digital noise ISO 1600, or authentic analog film grain (Kodak Portra 400, Tri-X 400, CineStill 800T halation).
- **Camera Angle & Elevation**: Eye-level, low-angle worm's-eye, high-angle bird's-eye, 90° flat lay top-down, Dutch tilt angle, or 30° isometric perspective.

### 3. Lighting Architecture & Atmosphere
- **Lighting Scenario**: Studio 3-point, natural window diffused, dramatic chiaroscuro, high-key commercial, low-key moody, cyberpunk dual-rim, golden hour sunset.
- **Key Light**: Source, direction (e.g., 45° camera-left, high overhead), intensity, color temperature in Kelvin (e.g., 3200K warm tungsten, 5600K daylight, 7500K overcast cool).
- **Fill Light**: Reflector bounce, soft ambient fill, fill ratio (e.g., 1:1, 2:1, 4:1).
- **Rim / Kicker / Hair Light**: Edge separation, silhouette highlights, neon accent backlights.
- **Shadow Physics**: Contact shadows (ambient occlusion under objects), cast shadow length, shadow edge softness (hard direct vs feathered softbox falloff).
- **Atmospheric Medium**: Clear studio air, subtle haze, volumetric god rays (crepuscular rays), smoke, mist, or floating dust motes.

### 4. Graphic Design, 3D & 2D Elements
- **3D Render Style**: Claymorphism, glassmorphism (frosted glass, transmission, refraction IOR, roughness), chrome metallic, iridescent pearlescent, plastic matte, soft vinyl toy aesthetic.
- **2D Vectors & Badges**: Geometric shapes, squiggles, starbursts, highlighter strokes, callout arrows, pill badges.
- **UI Mockups & Device Frames**: Phone screen border, browser window header with red/yellow/green dots, code editor frame, social engagement bar (likes, shares, bookmark icon).

### 5. Verbatim Typography & Text Fidelity (Zero-Error Protocol)
- **Transcription Rule**: Transcribe every single visible character verbatim. Never summarize or omit micro-text (e.g., author handle, slide counter, tiny footers, CTA button text).
- **Typographic Taxonomy**:
  - `role`: "H1_Headline" | "H2_Subheadline" | "Body_Copy" | "Bullet_Item" | "CTA_Button" | "Badge_Label" | "Footer_Caption"
  - `verbatim_text`: Exact text with identical spelling and punctuation.
  - `font_classification`: Geometric Sans (e.g., Inter, Montserrat, Gilroy), Humanist Sans, High-Contrast Editorial Serif (e.g., Playfair, Ogg), Neo-Brutalist Monospace, Bold Display.
  - `font_weight`: Thin (100), Regular (400), SemiBold (600), Bold (700), Heavy/Black (900).
  - `casing`: UPPERCASE, Title Case, lowercase, Sentence case.
  - `color_hex`: Exact font color hex code.
  - `spatial_anchor`: Coordinate position (e.g., "Top-Left quadrant [x: 10%, y: 15%]", "Centered Hero").
  - `special_effects`: Drop shadow, outer glow, gradient fill, 3D extrusion, stroke outline.

### 6. Color System & Hex Palette
- Extract 5 to 8 accurate Hex codes:
  - `primary_brand`: Main visual anchor.
  - `secondary_brand`: Supporting tone.
  - `accent_highlight`: Attention-grabbing neon/vibrant pop.
  - `background_surface`: Canvas base color or gradient endpoints.
  - `typography_contrast`: Dark mode vs light mode font colors.

---

## Output Format Specification

The response must always provide the structured JSON first, followed by the master replica text prompt.

```json
{
  "project_metadata": {
    "visual_type": "single_graphic | multi_slide_carousel | editorial_photo | 3d_render | ui_infographic",
    "total_slides": 1,
    "current_slide_index": 1,
    "aspect_ratio": "4:5",
    "target_dimensions": "1080x1350",
    "aesthetic_genre": "Minimalist High-Tech Corporate | Cyberpunk | Luxury Editorial | Notion-Style 3D"
  },
  "global_brand_tokens": {
    "color_palette": {
      "primary": "#0A0F1D",
      "secondary": "#1E293B",
      "accent_cyan": "#00F2FE",
      "accent_purple": "#7928CA",
      "background": "#05070E",
      "text_primary": "#FFFFFF",
      "text_secondary": "#94A3B8"
    },
    "typography_system": {
      "headline_font": "Bold Geometric Modern Sans-Serif, high tracking",
      "body_font": "Clean Neutral Sans-Serif, high legibility",
      "accent_font": "Monospace or Script"
    }
  },
  "slides": [
    {
      "slide_number": 1,
      "slide_purpose": "Hook / Title Slide / Value Delivery / CTA",
      "composition_and_layout": {
        "layout_style": "Split-horizontal | Centered Hero | Left-aligned Content Grid",
        "negative_space_ratio": "45%",
        "z_layers": {
          "layer_0_background": "Deep obsidian dark mode background with a subtle radial gradient glow (#00F2FE at 8% opacity) centered behind the primary subject.",
          "layer_1_ambient": "Subtle 2D isometric grid pattern with 10% opacity in top-right corner.",
          "layer_2_midground_hero": "Photorealistic floating 3D frosted glass prism with iridescent internal refractions, casting a soft ambient shadow downward.",
          "layer_3_overlays": "A floating neon pill tag with 1px border at top-left reading 'AI REVOLUTION'.",
          "layer_4_text": "Large bold title aligned left, subtitle directly beneath, swipe arrow icon bottom right.",
          "layer_5_post_processing": "Cinematic fine film grain, subtle anamorphic glow on highlights."
        }
      },
      "photographic_and_rendering_physics": {
        "camera_body": "Hasselblad H6D-100c Medium Format",
        "lens": "85mm prime lens",
        "camera_angle": "Eye-level straight-on with a subtle 5-degree upward tilt",
        "shot_distance": "Medium close-up",
        "aperture": "f/2.0 shallow depth of field with soft creamy circular bokeh",
        "shutter_speed": "1/500s sharp freeze",
        "iso_grain": "Clean ISO 100 with ultra-subtle analog film texture"
      },
      "lighting_setup": {
        "lighting_type": "Studio Chiaroscuro with Neon Rim Accents",
        "key_light": "Diffused softbox 45-degrees camera-left, neutral daylight 5500K",
        "fill_light": "Gentle bounce fill camera-right at 25% power",
        "rim_light": "High-intensity cyan kicker light at 135-degrees camera-back",
        "shadows": "Soft feathered contact shadows, smooth gradient falloff",
        "reflections": "Subtle glossy reflections on floor surface"
      },
      "graphic_and_3d_elements": [
        {
          "element_name": "Hero 3D Icon",
          "type": "3D Glassmorphism Geometric Shape",
          "materials": "Frosted glass, index of refraction 1.52, roughness 0.15, internal volumetric cyan glow",
          "position": "Center-right quadrant",
          "shadow": "Soft diffuse contact shadow below"
        }
      ],
      "verbatim_typography": {
        "text_elements": [
          {
            "role": "H1_Headline",
            "verbatim_text": "TURN ANY IMAGE INTO PERFECT JSON",
            "font_style": "Geometric Sans-Serif, Extra-Bold 800 weight",
            "casing": "ALL_CAPS",
            "color_hex": "#FFFFFF",
            "position": "Top-left quadrant, aligned with 10% canvas margin",
            "effects": "Subtle soft drop shadow rgba(0,0,0,0.4)"
          },
          {
            "role": "H2_Subheading",
            "verbatim_text": "For 100% Consistent Brand Visuals Across All Platforms",
            "font_style": "Modern Sans-Serif, Medium 500 weight",
            "casing": "Title Case",
            "color_hex": "#94A3B8",
            "position": "Directly below H1 headline with 24px vertical gap"
          },
          {
            "role": "Badge_Pill",
            "verbatim_text": "NEW WORKFLOW",
            "font_style": "Bold Sans-Serif 700, small caption size",
            "casing": "UPPERCASE",
            "color_hex": "#00F2FE text on #0E2238 pill container with #00F2FE 1px border",
            "position": "Above H1 headline at top-left"
          },
          {
            "role": "Slide_Counter",
            "verbatim_text": "01 / 07",
            "font_style": "Monospace, Regular 400",
            "casing": "NUMERIC",
            "color_hex": "#64748B",
            "position": "Top-right corner"
          },
          {
            "role": "Footer_CTA",
            "verbatim_text": "SWIPE TO REPLICATE →",
            "font_style": "Bold Sans-Serif, 600 weight",
            "casing": "UPPERCASE",
            "color_hex": "#38BDF8",
            "position": "Bottom-right corner aligned with bottom margin"
          }
        ]
      },
      "master_replica_text_prompt": "A high-end editorial social media carousel slide, aspect ratio 4:5, minimalist high-tech corporate aesthetic. Dark obsidian base background (#05070E) with subtle radial cyan glow (#00F2FE) behind a floating 3D frosted glass prism with iridescent refractions in the center-right. In the top-left, a cyan pill badge reading 'NEW WORKFLOW'. Below it, bold geometric uppercase headline reading 'TURN ANY IMAGE INTO PERFECT JSON' in crisp white (#FFFFFF) with subtle drop shadow, followed by subheadline in medium gray (#94A3B8) reading 'For 100% Consistent Brand Visuals Across All Platforms'. Top-right shows slide counter '01 / 07'. Bottom-right features an accent call-to-action reading 'SWIPE TO REPLICATE →' in vibrant cyan (#38BDF8). Shot with Hasselblad H6D-100c, 85mm lens, f/2.0 shallow depth of field, studio chiaroscuro lighting with softbox key and vivid cyan rim lighting, clean ISO 100 with fine analog film grain, hyper-detailed commercial render."
    }
  ]
}
```

---

## Master Replica Text Prompt Rules
When generating the `master_replica_text_prompt`:
1. **Verbatim Text Inside Quotes**: Enclose all written words inside single or double quotes (e.g. `reading 'HEADLINE TEXT'`).
2. **Specify Physical Gear**: Explicitly name the camera body, lens focal length, aperture f-stop, and lighting rig.
3. **Color Precision**: Name the exact color hex codes and gradient directions in natural language.
4. **Target Model Optimization**: The prompt is engineered to work reliably on Flux.1 Pro/Schnell, Midjourney v6.1 (with `--ar 4:5 --v 6.1 --style raw`), Ideogram 2.0 (for premier text typography rendering), and DALL-E 3.

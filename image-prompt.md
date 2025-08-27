```
Prompt Share: Colored Pencil on Kraft Paper

A colored pencil drawing of [SUBJECT] on brown kraft paper, using soft layering and paper tone for natural midtones, with vibrant highlights and subtle texture.

MJ with my --p style
```

```
ChatGPT-4o Prompt 👇

Design a bold and dynamic vector icon of [✌️], in a high-contrast color palette: pure black, white, and neon green. The style is playful, expressive, and energetic, with thick black outlines, exaggerated forms, and cartoon-like proportions. Add dynamic shadows and minimalistic graphic effects to create a strong visual impact. The design should feel fun, lively, slightly rebellious, and tech-inspired. No gradients, no textures — only flat colors and striking contrast.
```

```
ChatGPT-4o Prompt 👇

{
  "task": "Transform a user-uploaded portrait into a premium stylized 3D floating head for avatar/profile use",
  "style": {
    "goal": "Match the collectible 3D avatar aesthetic — floating head only, minimal background, fun accessories, premium look",
    "render_engine": "Cinema 4D + Redshift equivalent",
    "materials": {
      "skin": {
        "texture": "Soft matte with light pore detail, subtle subsurface scattering, slight gloss on cheeks and nose",
        "finish": "Stylized sculpted — clean and premium, not hyper-realistic or cartoonish"
      },
      "hair": {
        "material": "Sculpted strands with soft specular highlights",
        "finish": "Clean shapes, defined flow, no noise or over-detail"
      },
      "eyes": {
        "material": "Glossy stylized with subtle iris detail and clear reflections",
        "style": "Not photorealistic — bright and expressive with stylized shine"
      },
      "accessories": {
        "allowed": true,
        "types": ["bucket hat", "headphones", "glasses", "earring"],
        "rules": "Accessories can include fun stickers, emojis, or decorative elements for a stylish and energetic feel"
      }
    }
  },
  "geometry": {
    "pose": "Frontal centered view",
    "composition": "Only the head — no neck, no torso, floating silhouette",
    "expression": "Light smile or calm neutral depending on input image",
    "proportions": "Slightly stylized for charm — clean symmetry, soft features"
  },
  "background": {
    "type": "Solid or smooth gradient",
    "colors": ["light blue", "soft lavender", "peach", "pastel pink", "butter yellow"],
    "rules": "No text, no patterns, no icons — just a clean backdrop for the floating head"
  },
  "render": {
    "resolution": "2048x2048px or higher",
    "format": "PNG with transparent or soft pastel background",
    "lighting": {
      "type": "Soft three-point studio lighting",
      "mood": "Warm and clean — slight rim light for definition"
    },
    "camera": {
      "angle": "Perfect frontal portrait view",
      "lens": "Portrait-style with background separation"
    },
    "output_rules": {
      "composition": "Tightly cropped to floating head only",
      "shadow": "Subtle soft base shadow allowed under head",
      "material_consistency": "Match high-quality stylized references — not flat cartoon, not hyperreal"
    }
  },
  "output_goals": {
    "use_case": "Digital profile avatar — collectible, cool, and instantly recognizable",
    "style_consistency": "Match references like Bucket Hat Girl, Gaming Headphones Guy, and Emoji Glasses Girl"
  },
  "input_requirements": {
    "photo": "Frontal or 3/4 angle, clean lighting, minimal background",
    "expression": "Prefer neutral or slight smile",
    "accessory guidance": "Auto-add stylish accessories and stickers based on personality and vibe"
  }
}
```

```json
{
    "task": "Generate a premium 3D cartoon flat travel icon with grouped objects.",
    "style": {
        "goal": "Match the collectible clay-molded icon aesthetic — smooth, rounded shapes, soft matte texture, warm pastel colors, playful yet premium look",
        "render_engine": "Cinema 4D + Redshift equivalent with soft GI lighting",
        "materials": {
            "clay": {
                "texture": "Matte, smooth, with subtle handcrafted imperfections",
                "finish": "Sculpted and slightly stylized — not photorealistic, not flat cartoon"
            },
            "details": {
                "material": "Matte painted clay with clean color separation",
                "finish": "Consistent saturation, no noise or rough edges"
            },
            "shadows": {
                "type": "Soft ambient occlusion with light contact shadows",
                "style": "Minimal but grounding"
            }
        }
    },
    "geometry": {
        "pose": "Frontal centered view for each icon",
        "composition": "Single object per icon, isolated, no overlapping elements",
        "arrangement": "Uniform grid layout, consistent icon proportions, equal spacing between icons",
        "perspective": "Orthographic-like with slight top-down angle for depth"
    },
    "background": {
        "type": "Solid light neutral color",
        "colors": [
            "soft beige",
            "light cream",
            "pastel off-white"
        ],
        "rules": "No patterns, no gradients, no text — clean background for icon clarity"
    },
    "render": {
        "resolution": "1024x1024px per icon or higher",
        "format": "PNG with transparent or solid light background",
        "lighting": {
            "type": "Soft diffused studio lighting",
            "mood": "Warm, clean, and inviting"
        },
        "camera": {
            "angle": "Straight-on or slightly elevated view",
            "lens": "Minimal distortion for consistent icon scale"
        },
        "output_rules": {
            "composition": "All icons should be visually balanced and consistent in style",
            "shadow": "Subtle soft shadows allowed under each object",
            "material_consistency": "Match high-quality clay-style references — avoid flat vector or hyperreal textures"
        }
    },
    "output_goals": {
        "use_case": "Travel-related app UI, infographics, or themed sticker pack",
        "style_consistency": "Match cohesive clay-style set with warm, inviting colors and consistent shapes"
    },
    "input_requirements": {
        "objects": [
          { "main": "Tent", "lamp": "Lantern", "moon": "Crescent Moon", "ground": "Grass" },
          { "main": "Backpack", "straps": "Red Straps", "pocket": "Front Pocket" },
          { "main": "Hot Air Balloon", "balloon": "Striped Balloon", "basket": "Basket" },
          { "main": "Map", "pin": "Location Pin", "mountains": "Landscape Drawing" },
          { "main": "Snorkel Mask", "tube": "Snorkel Tube", "goggles": "Mask Lens" },

          { "main": "Bottle", "inside": "Message Scroll", "leaf": "Green Leaf" },
          { "main": "Kayak", "paddle": "Double Paddle", "waves": "Water Waves" },
          { "main": "Eiffel Tower", "flag": "Red Flag", "tree": "Tree" },
          { "main": "Cooler Box", "lock": "Padlock", "handle": "Handle" },
          { "main": "Taxi", "face": "Smile Face", "sign": "Taxi Sign" },

          { "main": "Camera", "photo": "Printed Photo", "lens": "Lens" },
          { "main": "Bicycle", "lock": "Padlock Sign", "frame": "Bike Frame" },
          { "main": "Signpost", "signs": "Hiking Arrows", "base": "Pole" },
          { "main": "Compass", "needle": "Arrow Needle", "maps": "Mini Maps" },
          { "main": "Lighthouse", "cloud": "Cloud", "leaf": "Small Plant" },

          { "main": "Beach Ball", "stripes": "Colored Stripes", "pump": "Air Valve" },
          { "main": "Boots", "laces": "Shoelaces", "pair": "Two Boots" },
          { "main": "Postcard", "stamp": "Postage Stamp", "envelope": "Envelope" },
          { "main": "Surfboard", "hat": "Straw Hat", "shell": "Seashell" },
          { "main": "Fishing Rod", "line": "Fishing Line", "hook": "Hook", "fish": "Green Fish" }
        ],
        "color_palette": [
          "bright orange",
          "burnt orange",
          "peach orange",
          "golden yellow",
          "pale yellow",
          "olive green",
          "light green",
          "mint green",
          "forest green",
          "sky blue",
          "light blue",
          "teal blue",
          "aqua blue",
          "soft red",
          "coral red",
          "brown",
          "light brown",
          "beige",
          "ivory",
          "white",
          "light gray",
          "dark gray",
          "black"
        ],
        "icon_rules": "Each icon represents a single concept clearly without unnecessary background elements"
    }
}
```

```
render engine:
	Cinema 4D: '动态图形和广告行业'
	Blender: '通用'
	Autodesk Maya: '电影'
```


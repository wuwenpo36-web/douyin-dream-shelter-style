# GPT Image Prompt Contract

Use this reference whenever the user asks for a GPT Image prompt, a cover prompt, a white-background asset, a first-person still, or an image-edit prompt.

## Contents

- Required response shape
- Generation modes
- Reference-role discipline
- Prompt order
- First-person anatomy
- Branded objects and exact text
- White-background assets and multi-view sheets
- Editing contract
- Common prompt repairs

## Required Response Shape

Return one copyable English prompt unless the user requests another language.

Do not split prohibitions into a separate negative-prompt section for this user's workflow. End the same prompt with an integrated sentence such as “Do not add…” or “Avoid…”.

If the user says “直接给我 prompt”, output only the prompt without commentary, headings, options, or explanation.

State the requested ratio inside the prompt: vertical 9:16, portrait 3:4, landscape 4:3, or another explicit format.

## Generation Modes

Choose one mode before writing:

### Pure Text-To-Image

Use when no image will be uploaded, or when the user says an image is only an error example. Do not write “use the reference image,” “Image 1,” or “preserve the uploaded image.” Reconstruct every required visual fact in text.

### Reference-Guided Generation

Use when uploaded images provide scene, construction, product detail, scale, or design identity but the final image is new. Assign each image a single job.

### Image Edit

Use when the user wants the existing image preserved except for a specific change. Begin with “Edit the uploaded image with minimal changes only.” Then state the target change and a strict preservation lock.

## Reference-Role Discipline

Define roles explicitly:

- Image 1: base scene, camera, weather, and composition;
- Image 2: object, product, or shelter construction;
- Image 3: scale relationship only;
- Image 4: character, creature, or motif construction;
- mood image: color and atmosphere only, not a frame to copy;
- error example: never referenced in the final prompt if it will not be uploaded.

Do not blend roles ambiguously. If one image supplies product packaging, require exact packaging fidelity but do not import its white background into the final scene.

## Prompt Order

Use this order for reliable results:

1. format and realism level;
2. camera and POV;
3. base location and time;
4. primary subject-action relationship;
5. shelter or object placement and scale;
6. anatomy and pose;
7. weather and physical effects;
8. materials and fine details;
9. lighting sources and color contrast;
10. exact text or packaging requirements;
11. preservation locks or integrated prohibitions.

Put the most important spatial relationship early. Examples: “a gigantic shelter occupies the lower-left cliff below the viewer,” or “the waterfall fills the forward-left half of the route and lies directly in the climber's path.”

## First-Person Anatomy

Use “true first-person human eye-level POV” and describe a real posture.

- Show at most two natural forearms or hands.
- Show a portion of torso and legs only if visible from that posture.
- Keep limb lengths normal, shoulders implied, joints connected, and hand count exact.
- Anchor the body to a board, saddle, handlebars, rope system, seat, floor, or slide.
- Use realistic foreshortening rather than a wide-angle body stretched across the frame.

Explicitly avoid detached limbs, extra hands, duplicated legs, extreme arm length, malformed fingers, floating equipment, chest-level camera, ankle-level camera, or third-person views.

## Branded Objects And Exact Text

For products or packaging:

- require exact construction, colors, label placement, cap, proportions, and material;
- specify real-world hand scale when the product is held;
- keep the label facing camera only when physically plausible;
- place literal required wording in quotation marks;
- say the wording must be fully legible, correctly oriented, and not paraphrased;
- prohibit invented slogans, extra logos, and gibberish.

For Chinese text, repeat only the approved literal string. If the source image itself is unclear, do not guess; tell the prompt to reproduce the supplied artwork faithfully.

## White-Background Assets And Multi-View Sheets

Use a seamless pure-white background, not a gray studio, floor horizon, gradient, showroom, or environmental set.

Allow only a soft natural contact shadow beneath the object. Keep the entire object inside frame with generous white margins.

For a three-view sheet:

- use front, side, and top or rear views as requested;
- keep identical geometry, scale, windows, doors, wheels, bands, and markings across views;
- use orthographic or near-orthographic views;
- align the views cleanly;
- do not add extra concept variants.

For giant shelter assets, use tiny human-scale doors, normal windows, repeated levels, railings, and service details to prove size even on white.

## Editing Contract

Use this pattern:

“Edit the uploaded image with minimal changes only. [Exact target edit]. Match the existing perspective, scale, material, lighting, reflections, shadows, depth of field, and color grade. Preserve [camera, crop, architecture, people, furniture, weather, text, and all unrelated details] exactly as they are. Do not [integrated prohibitions].”

If removing an object, reconstruct the surface behind it instead of leaving a blur, hole, duplicate seam, or ghost shadow.

If replacing text, change only the specified panel or package face. Preserve its perspective, print texture, fold, surface wear, and occlusion.

## Common Prompt Repairs

- **Scene too close:** specify camera-to-subject distance, retain surrounding environment, and prevent the subject from filling the frame.
- **Shelter too small:** add multiple floors and normal-scale doors/windows; reduce the entry-door proportion.
- **Shelter too toy-like:** require real architecture, buildable structure, weathered only as appropriate, and physically plausible materials.
- **Room too dark:** name warm practical sources and readable target illumination; keep shadow detail.
- **Room too empty:** add built-ins, alcoves, useful facilities, textiles, plants, and one layered focal zone—not random props.
- **Room too cramped:** preserve a clear walking route and reduce foreground furniture size.
- **Too much glass:** replace wall-to-wall glazing with one controlled reinforced window in a deep reveal.
- **Too colorful:** limit to one main and two secondary hues; use lightly tinted transparent glass without patterns.
- **Reference mistakenly invoked:** remove all image-number language and rewrite as pure text-to-image.
- **White background looks gray:** say “uniform seamless pure white (#FFFFFF), no gray gradient, no visible studio floor or horizon.”

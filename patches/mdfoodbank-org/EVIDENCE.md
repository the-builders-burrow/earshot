# Earshot — accessibility remediation proposal for https://mdfoodbank.org/

**This is a reviewable patch proposal with verification evidence, not a compliance claim.** Earshot flags what it cannot determine instead of guessing. An agent proposes; a human disposes — nothing here should be read as "compliant" or "fully accessible."

Target: https://mdfoodbank.org/
Scanned: 2026-07-24T22:43:03.496Z

## What this PR is and isn't

This diffs a snapshot of the fetched HTML against Earshot's proposed DOM mutations for https://mdfoodbank.org/. **It is not a pull request against that site's actual source repository** — we don't have access to it. It's a reviewable proposal in the shape a real PR would take, for the site owner or for demo purposes, opened against this repo.

## Grader A — axe-core violations

Before: **59**
After: **63**
Removed keys: aria-allowed-attr::#slick-slide02, aria-hidden-focus::#slick-slide00, presentation-role-conflict::#slick-slide02
Added keys (should be empty — the verifier reverts any fix that adds one): aria-allowed-attr::#slick-slide00, aria-hidden-focus::#slick-slide02, aria-valid-attr-value::#slick-slide00, color-contrast::.et_pb_button.et_pb_more_button[target="_blank"], color-contrast::.et_pb_slide_1 > .et_pb_container.clearfix > .et_pb_slider_container_inner > .et_pb_slide_description > .et_pb_slide_content > p, color-contrast::.et_pb_slide_1 > .et_pb_container.clearfix > .et_pb_slider_container_inner > .et_pb_slide_description > .et_pb_slide_title > a, presentation-role-conflict::#slick-slide00

## Grader B — narration comprehension

Before: 4/5 — The primary tasks (donating, finding food, signing up) are clearly labeled and accessible. However, several elements lack labels or context (unlabeled links, number links, unlabeled listbox), which could confuse users navigating by screen reader. The redundant link text in cards and news items may also cause verbosity, but does not block task completion. Overall, the page is mostly usable with minor clarity issues.
After: 4/5 — The primary task of donating is clearly accessible via the 'Give Monthly' and 'Donate' links. Most interactive elements are labeled, but unlabeled links and ambiguous carousel controls may cause confusion in secondary sections, preventing a perfect score.

## Patches proposed (26)

- ↩ reverted — setAttribute #menu-mfb-utility-navigation — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute label[for="mainSearchInput"] — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute #mainSearchInput — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute #mainSearch > .silc-offcanvas__trigger[href$="#mainSearch"] — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .header__logo — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .section--footer-tier1 — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .section--footer-tier2 > .compartment > .compartment--inner > .silc-grid > .silc-grid__col--3-800.silc-grid__col--6-600.silc-grid__col — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute strong — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .custom-html-widget.textwidget > .gf_browser_gecko.gform_wrapper.gform_legacy_markup_wrapper > form[method="post"][enctype="multipart/form-data"][action="/"] > .gform-body.gform_body > .gform_fields.form_sublabel_below.description_below > .gfield--type-text.gfield--input-type-text.gfield:nth-child(1) > .ginput_container_text.ginput_container — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .custom-html-widget.textwidget > .gf_browser_gecko.gform_wrapper.gform_legacy_markup_wrapper > form[method="post"][enctype="multipart/form-data"][action="/"] > .gform-body.gform_body > .gform_fields.form_sublabel_below.description_below > .gfield--width-full.gfield--type-text.gfield--input-type-text > .ginput_container_text.ginput_container — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .custom-html-widget.textwidget > .gf_browser_gecko.gform_wrapper.gform_legacy_markup_wrapper > form[method="post"][enctype="multipart/form-data"][action="/"] > .gform-body.gform_body > .gform_fields.form_sublabel_below.description_below > .gfield--type-email.gfield--input-type-email.gfield > .ginput_container_email.ginput_container — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .silc-grid__col--4-800 — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .section--footer-tier3 — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .st-total — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .st-first — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute div[data-network="facebook"] — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute div[data-network="twitter"] — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute div[data-network="whatsapp"] — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .st-last — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .st-toggle > .st-right — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute iframe[title="reCAPTCHA"] — Content outside landmarks needs a navigable region; role=main is the smallest demo fix. (reverted after verification regression)
- ↩ reverted — setAttribute .et-pb-arrow-prev — Add aria-label to provide an accessible name for the link (reverted after verification regression)
- ↩ reverted — setAttribute .et-pb-arrow-next — Add an explicit aria-label matching the visible link text to ensure a discernible name for screen readers. (reverted after verification regression)
- ↩ reverted — setAttribute .et_pb_blurb_0 > .et_pb_blurb_content > .et_pb_main_blurb_image > a[href$="approach/"] — Derived from the link target indicating the page about the approach to hunger in Maryland (reverted after verification regression)
- ↩ reverted — setAttribute .et_pb_blurb_1 > .et_pb_blurb_content > .et_pb_main_blurb_image > a[href$="approach/"] — Derived from the link target indicating the page about the approach to hunger in Maryland (reverted after verification regression)
- ↩ reverted — setAttribute .et_pb_blurb_2 > .et_pb_blurb_content > .et_pb_main_blurb_image > a[href$="approach/"] — Derived from the link target indicating the page about the approach to hunger in Maryland (reverted after verification regression)

## Flagged for human review (3)

A good flag rate is a feature — every item below is something the model declined to guess at.

- `aria-required-children` .slick-dots — The tablist contains children with role='presentation', which is not allowed. The children need to be changed to role='tab', but we cannot modify child elements from this context.: The violation requires modifying child elements, which is not possible with a single attribute change on the parent.
- `heading-order` .et_pb_blurb_0 > .et_pb_blurb_content > .et_pb_blurb_container > h4 — Heading order issues require document restructuring, not a single attribute fix.: The heading order violation cannot be fixed with a single attribute; it requires changing the heading level or restructuring the document.
- `heading-order` #custom_html-2 > .custom-html-widget.textwidget > div[itemscope=""] > h5 — Heading order violation requires structural change, not a single attribute fix.: The heading is an h5, which likely skips a level; fixing it requires changing the heading element itself, not just an attribute.

## Narration diff (before → after)

```diff
--- patches/mdfoodbank-org/before-narration.txt	2026-07-24 15:43:03
+++ patches/mdfoodbank-org/after-narration.txt	2026-07-24 15:43:03
@@ -21,10 +21,10 @@
 heading level 1, "Give Monthly To Help All Year Long"
 text, "Every $1 helps provide a meal for neighbors."
 link, "Give Monthly"
-heading level 2, "Find Food Near You"
-link, "Find Food Near You"
-text, "If you need food, please use this map to find an open partner in your community. We are updating the map on a regular basis, but please call the partner first …"
-link, "Find Food"
+heading level 2, "Start Your Virtual Food Drive"
+link, "Start Your Virtual Food Drive"
+text, "Empower your community to help hungry Marylanders in just a few clicks."
+link, "Start Today"
 link, "4"
 link, "5"
 link, "1"
@@ -89,14 +89,14 @@
 listbox, unlabeled
 option, "CareFirst BlueCross BlueShield"
 image, "CareFirst BlueCross BlueShield"
+option, "CareFirst BlueCross BlueShield"
+image, "CareFirst BlueCross BlueShield"
 option, "Gilead Foundation logo"
 image, "Gilead Foundation logo"
 option, "CareFirst BlueCross BlueShield"
 image, "CareFirst BlueCross BlueShield"
-option, "CareFirst BlueCross BlueShield"
-image, "CareFirst BlueCross BlueShield"
 button, "Next"
-button, "3"
+button, "2"
 link, "Maryland Food Bank"
 image, "Maryland Food Bank"
 link, " Facebook"

```

## HTML diff (snapshot before → after mutation)

```diff
--- patches/mdfoodbank-org/before.html	2026-07-24 15:43:03
+++ patches/mdfoodbank-org/after.html	2026-07-24 15:43:03
@@ -756,9 +756,9 @@
 				
 				
 				
-				<div class="et_pb_module et_pb_slider et_pb_slider_0 et_pb_slider_fullwidth_off et_slider_auto et_slider_speed_7000 et_slider_auto_ignore_hover et_pb_slider_show_image et_pb_bg_layout_dark" data-active-slide="et_pb_slide_0">
+				<div class="et_pb_module et_pb_slider et_pb_slider_0 et_pb_slider_fullwidth_off et_slider_auto et_slider_speed_7000 et_slider_auto_ignore_hover et_pb_slider_show_image et_pb_bg_layout_dark et_slide_transition_to_next" data-active-slide="et_pb_slide_0">
 				<div class="et_pb_slides">
-					<div class="et_pb_slide et_pb_slide_0 et_clickable et_pb_bg_layout_dark et_pb_slide_with_image et_pb_media_alignment_center et-pb-active-slide" data-slide-id="et_pb_slide_0">
+					<div class="et_pb_slide et_pb_slide_0 et_clickable et_pb_bg_layout_dark et_pb_slide_with_image et_pb_media_alignment_center et-pb-active-slide" data-slide-id="et_pb_slide_0" style="z-index: 1; display: block; opacity: 0.94448;">
 				
 				
 				<div class="et_pb_container clearfix" style="height: 331.781px;">
@@ -774,12 +774,12 @@
 				
 				
 			</div>
-			<div class="et_pb_slide et_pb_slide_1 et_clickable et_pb_bg_layout_dark et_pb_slide_with_image et_pb_media_alignment_center" data-slide-id="et_pb_slide_1">
+			<div class="et_pb_slide et_pb_slide_1 et_clickable et_pb_bg_layout_dark et_pb_slide_with_image et_pb_media_alignment_center et-pb-moved-slide et_slide_transition" data-slide-id="et_pb_slide_1" style="z-index: 2; display: list-item; opacity: 0.05552;">
 				
 				
 				<div class="et_pb_container clearfix" style="height: 331.781px;">
 					<div class="et_pb_slider_container_inner">
-						<div class="et_pb_slide_image"><img decoding="async" width="1920" height="1080" data-src="https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse.jpg" alt="" data-srcset="https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse.jpg 1920w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-300x169.jpg 300w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1024x576.jpg 1024w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-768x432.jpg 768w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1536x864.jpg 1536w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1080x608.jpg 1080w" data-sizes="(max-width: 1920px) 100vw, 1920px" class="wp-image-49691 lazyload" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMSIgaGVpZ2h0PSIxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjwvc3ZnPg==" style="--smush-placeholder-width: 1920px; --smush-placeholder-aspect-ratio: 1920/1080;"></div>
+						<div class="et_pb_slide_image" style="margin-top: -132.5px;"><img decoding="async" width="1920" height="1080" data-src="https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse.jpg" alt="" data-srcset="https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse.jpg 1920w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-300x169.jpg 300w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1024x576.jpg 1024w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-768x432.jpg 768w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1536x864.jpg 1536w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1080x608.jpg 1080w" data-sizes="(max-width: 1920px) 100vw, 1920px" class="wp-image-49691 lazyloaded" src="https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse.jpg" style="--smush-placeholder-width: 1920px; --smush-placeholder-aspect-ratio: 1920/1080; max-height: 265.425px;" sizes="(max-width: 1920px) 100vw, 1920px" srcset="https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse.jpg 1920w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-300x169.jpg 300w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1024x576.jpg 1024w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-768x432.jpg 768w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1536x864.jpg 1536w, https://mdfoodbank.org/wp-content/uploads/2025/10/blogfull-contents-of-Maryland-Food-Banks-Holiday-Meal-Kit-on-display-in-our-warehouse-1080x608.jpg 1080w"></div>
 						<div class="et_pb_slide_description">
 							<h2 class="et_pb_slide_title"><a href="https://mdfoodbank.funraise.org/">Start Your Virtual Food Drive</a></h2><div class="et_pb_slide_content"><p>Empower your community to help hungry Marylanders in just a few clicks.</p></div>
 							<div class="et_pb_button_wrapper"><a class="et_pb_button et_pb_more_button" href="https://mdfoodbank.funraise.org/" target="_blank">Start Today</a></div>
@@ -793,7 +793,7 @@
 			
 				</div>
 				
-			<div class="et-pb-slider-arrows"><a class="et-pb-arrow-prev" href="#"><span>Previous</span></a><a class="et-pb-arrow-next" href="#"><span>Next</span></a></div><div class="et-pb-controllers"><a href="#" class="et-pb-active-control">1</a><a href="#">2</a></div></div>
+			<div class="et-pb-slider-arrows"><a class="et-pb-arrow-prev" href="#"><span>Previous</span></a><a class="et-pb-arrow-next" href="#"><span>Next</span></a></div><div class="et-pb-controllers"><a href="#" class="et-pb-active-control">1</a><a href="#" class="">2</a></div></div>
 			
 			</div>
 				
@@ -1208,7 +1208,7 @@
 				
 				
 				
-				<div aria-live="polite" class="slick-list draggable"><div class="slick-track" style="opacity: 1; width: 5066px; transform: translate3d(-1788px, 0px, 0px);" role="listbox"><div class="et_pb_module et_pb_blurb et_pb_blurb_8 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-cloned" data-slick-index="-4" id="" aria-hidden="true" style="width: 298px;" tabindex="-1">
+				<div aria-live="polite" class="slick-list draggable"><div class="slick-track" style="opacity: 1; width: 5066px; transform: translate3d(-2682px, 0px, 0px);" role="listbox"><div class="et_pb_module et_pb_blurb et_pb_blurb_8 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-cloned" data-slick-index="-4" id="" aria-hidden="true" style="width: 298px;" tabindex="-1">
 				
 				
 				
@@ -1280,7 +1280,7 @@
 						
 					</div>
 				</div>
-			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_5 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-current slick-active" data-slick-index="2" aria-hidden="false" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide02">
+			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_5 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide" data-slick-index="2" aria-hidden="true" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide02">
 				
 				
 				
@@ -1292,7 +1292,7 @@
 						
 					</div>
 				</div>
-			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_6 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-active" data-slick-index="3" aria-hidden="false" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide03">
+			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_6 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide" data-slick-index="3" aria-hidden="true" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide03">
 				
 				
 				
@@ -1304,7 +1304,7 @@
 						
 					</div>
 				</div>
-			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_7 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-active" data-slick-index="4" aria-hidden="false" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide04">
+			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_7 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide" data-slick-index="4" aria-hidden="true" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide04">
 				
 				
 				
@@ -1316,7 +1316,7 @@
 						
 					</div>
 				</div>
-			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_8 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-active" data-slick-index="5" aria-hidden="false" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide05">
+			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_8 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-current slick-active" data-slick-index="5" aria-hidden="false" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide05">
 				
 				
 				
@@ -1328,7 +1328,7 @@
 						
 					</div>
 				</div>
-			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_9 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide" data-slick-index="6" aria-hidden="true" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide06">
+			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_9 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-active" data-slick-index="6" aria-hidden="false" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide06">
 				
 				
 				
@@ -1340,7 +1340,7 @@
 						
 					</div>
 				</div>
-			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_10 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide" data-slick-index="7" aria-hidden="true" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide07">
+			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_10 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-active" data-slick-index="7" aria-hidden="false" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide07">
 				
 				
 				
@@ -1352,7 +1352,7 @@
 						
 					</div>
 				</div>
-			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_11 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide" data-slick-index="8" aria-hidden="true" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide08">
+			</div><div class="et_pb_module et_pb_blurb et_pb_blurb_11 divilife-3-col-feature-blurb et_pb_text_align_left et_pb_blurb_position_top et_pb_bg_layout_light slick-slide slick-active" data-slick-index="8" aria-hidden="false" style="width: 298px;" tabindex="-1" role="option" aria-describedby="slick-slide08">
 				
 				
 				
@@ -1413,7 +1413,7 @@
 					</div>
 				</div>
 			</div></div></div>
-			<button type="button" data-role="none" class="slick-next slick-arrow" aria-label="Next" role="button" style="">Next</button><ul class="slick-dots" style="" role="tablist"><li class="" aria-hidden="true" role="presentation" aria-selected="true" aria-controls="navigation00" id="slick-slide00"><button type="button" data-role="none" role="button" tabindex="0">1</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation01" id="slick-slide01" class=""><button type="button" data-role="none" role="button" tabindex="0">2</button></li><li aria-hidden="false" role="presentation" aria-selected="false" aria-controls="navigation02" id="slick-slide02" class="slick-active"><button type="button" data-role="none" role="button" tabindex="0">3</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation03" id="slick-slide03"><button type="button" data-role="none" role="button" tabindex="0">4</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation04" id="slick-slide04"><button type="button" data-role="none" role="button" tabindex="0">5</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation05" id="slick-slide05"><button type="button" data-role="none" role="button" tabindex="0">6</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation06" id="slick-slide06"><button type="button" data-role="none" role="button" tabindex="0">7</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation07" id="slick-slide07"><button type="button" data-role="none" role="button" tabindex="0">8</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation08" id="slick-slide08"><button type="button" data-role="none" role="button" tabindex="0">9</button></li></ul></div>
+			<button type="button" data-role="none" class="slick-next slick-arrow" aria-label="Next" role="button" style="">Next</button><ul class="slick-dots" style="" role="tablist"><li class="" aria-hidden="true" role="presentation" aria-selected="true" aria-controls="navigation00" id="slick-slide00"><button type="button" data-role="none" role="button" tabindex="0">1</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation01" id="slick-slide01" class=""><button type="button" data-role="none" role="button" tabindex="0">2</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation02" id="slick-slide02" class=""><button type="button" data-role="none" role="button" tabindex="0">3</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation03" id="slick-slide03" class=""><button type="button" data-role="none" role="button" tabindex="0">4</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation04" id="slick-slide04" class=""><button type="button" data-role="none" role="button" tabindex="0">5</button></li><li aria-hidden="false" role="presentation" aria-selected="false" aria-controls="navigation05" id="slick-slide05" class="slick-active"><button type="button" data-role="none" role="button" tabindex="0">6</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation06" id="slick-slide06" class=""><button type="button" data-role="none" role="button" tabindex="0">7</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation07" id="slick-slide07" class=""><button type="button" data-role="none" role="button" tabindex="0">8</button></li><li aria-hidden="true" role="presentation" aria-selected="false" aria-controls="navigation08" id="slick-slide08" class=""><button type="button" data-role="none" role="button" tabindex="0">9</button></li></ul></div>
 				
 				
 				
@@ -1823,4 +1823,5 @@
     <img alt="arrow_right sharing button" src="https://platform-cdn.sharethis.com/img/arrow_right.svg">
   </div>
 </div></div><div><div class="grecaptcha-badge" data-style="bottomright" style="width: 256px; height: 60px; display: block; transition: right 0.3s; position: fixed; bottom: 14px; right: -186px; box-shadow: gray 0px 0px 5px; border-radius: 2px; overflow: hidden;"><div class="grecaptcha-logo"><iframe title="reCAPTCHA" width="256" height="60" role="presentation" name="a-5fxoslhn94wt" frameborder="0" scrolling="no" sandbox="allow-forms allow-popups allow-same-origin allow-scripts allow-top-navigation allow-modals allow-popups-to-escape-sandbox allow-storage-access-by-user-activation" src="https://www.google.com/recaptcha/api2/anchor?ar=1&amp;k=6LfCf6kUAAAAAL6dbMm2WH1oacB0Qx_J8A3Hr6Zp&amp;co=aHR0cHM6Ly9tZGZvb2RiYW5rLm9yZzo0NDM.&amp;hl=en&amp;v=A7KpaEASfhDcK0nXxgQEyyYv&amp;size=invisible&amp;anchor-ms=20000&amp;execute-ms=30000&amp;cb=2thk0gbesrgc"></iframe></div><div class="grecaptcha-error"></div><textarea id="g-recaptcha-response-100000" name="g-recaptcha-response" class="g-recaptcha-response" style="width: 250px; height: 40px; border: 1px solid rgb(193, 193, 193); margin: 10px 25px; padding: 0px; resize: none; display: none;"></textarea></div><iframe style="display: none;"></iframe></div><div id="batBeacon995164882112" style="width: 0px; height: 0px; display: none; visibility: hidden;"><img id="batBeacon312438896825" width="0" height="0" alt="" src="https://bat.bing.com/action/0?ti=139001359&amp;tm=gtm002&amp;Ver=2&amp;mid=7dfdef29-666f-48ab-b583-03bab618cd1d&amp;bo=1&amp;sid=bd2a69f087b011f1b90465d952bcf31c&amp;vid=bd2a7b9087b011f19ac9b9b7a7817f7a&amp;vids=1&amp;msclkid=N&amp;pi=0&amp;lg=en-US&amp;sw=1280&amp;sh=720&amp;sc=24&amp;nwd=1&amp;tl=Maryland%20Food%20Bank%20-%20A%20Hunger%20Relief%20Non-Profit%20%7C%20Donate%20Now&amp;p=https%3A%2F%2Fmdfoodbank.org%2F&amp;r=&amp;lt=2795&amp;evt=pageLoad&amp;sv=2&amp;cdb=AQAQ&amp;rn=399090" style="width: 0px; height: 0px; display: none; visibility: hidden;"></div>
-<script type="text/javascript" id="" charset="">cntrUpTag.track("cntrData","bc8d340db1365f81");</script><noscript><img width="1" height="1" src="//action.dstillery.com/orbserv/nspix?adv=cl176099641028679&amp;ns=9500&amp;nc=page_view&amp;ncv=51&amp;dstOrderId=&amp;dstOrderAmount="></noscript><iframe src="javascript:false" style="width: 0px; height: 0px; border: 0px; display: none !important;"></iframe></body></html>
\ No newline at end of file
+<script type="text/javascript" id="" charset="">cntrUpTag.track("cntrData","bc8d340db1365f81");</script><noscript><img width="1" height="1" src="//action.dstillery.com/orbserv/nspix?adv=cl176099641028679&amp;ns=9500&amp;nc=page_view&amp;ncv=51&amp;dstOrderId=&amp;dstOrderAmount="></noscript><iframe src="javascript:false" style="width: 0px; height: 0px; border: 0px; display: none !important;"></iframe><img height="1" width="1" style="border-style:none;" alt="" src="https://insight.adsrvr.org/track/pxl/?adv=8u96tm3&amp;ct=0:z8qzfvc&amp;fmt=3"><script id="" text="" charset="" type="text/javascript" src="//action.dstillery.com/orbserv/nsjs?adv=cl176099641028679&amp;ns=9500&amp;nc=15s_timer&amp;ncv=51&amp;dstOrderId=&amp;dstOrderAmount="></script><script type="text/javascript" id="" charset="">!function(b,e,f,g,a,c,d){b.fbq||(a=b.fbq=function(){a.callMethod?a.callMethod.apply(a,arguments):a.queue.push(arguments)},b._fbq||(b._fbq=a),a.push=a,a.loaded=!0,a.version="2.0",a.queue=[],c=e.createElement(f),c.async=!0,c.src=g,d=e.getElementsByTagName(f)[0],d.parentNode.insertBefore(c,d))}(window,document,"script","https://connect.facebook.net/en_US/fbevents.js");fbq("init","1235465568390841");fbq("track","PageView");</script>
+<noscript><img height="1" width="1" style="display:none" src="https://www.facebook.com/tr?id=1235465568390841&amp;ev=PageView&amp;noscript=1"></noscript><script type="text/javascript" id="" charset="">fbq("track","ViewContent");</script><noscript><img width="1" height="1" src="//action.dstillery.com/orbserv/nspix?adv=cl176099641028679&amp;ns=9500&amp;nc=15s_timer&amp;ncv=51&amp;dstOrderId=&amp;dstOrderAmount="></noscript></body></html>
\ No newline at end of file

```

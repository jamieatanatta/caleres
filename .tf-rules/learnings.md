## Consolidated

## Recent
[chat] Horizon badge is inside card-gallery capture (position: absolute over image). To place below image: render a second .product-badges--below-image div OUTSIDE the capture (after render 'card-gallery'), add display:none + position:static in block stylesheet, then show with section-scoped CSS
[chat] .product-badges--below-image must have position:static to override .product-badges { position: absolute } — both are 0,1,0 specificity so cascade order matters; place --below-image rule after the base .product-badges rule
[chat] product-title and price block font/font_size/case settings only apply when type_preset == 'custom' — for named presets (rte, h4, h5, h6 etc.) those settings are ignored; the preset class drives all typography
[chat] h5 preset = 14px Montserrat n5 (500 weight); h6 preset = 12px Montserrat n5 (500 weight); paragraph/rte = 14px Montserrat n4 (400 weight) — use h5 for product card text to get 14px medium weight
[chat] scheme-7 is the Circus red sale badge color scheme: background #cc2737, foreground #ffffff — set badge_sale_color_scheme to scheme-7 globally
[chat] Circus NY primary button color is #333232 (not the styleguide hot pink #e91e8c) — update primary/primary_hover/primary_button_* in all non-overlay color schemes (scheme-1 through scheme-5 plus UUID scheme); leave scheme-6 white buttons intact for hero overlays

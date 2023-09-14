view: viewf viewb

viewf: difference/front.jpg
	gwenview $<

viewb: difference/back.jpg
	gwenview $<

difference/%.jpg: drawings/%-drawn.jpg
	composite $< ./photos/$*.jpg -compose difference  ./difference/$*.jpg || true

drawings/front-drawn.jpg drawings/back-drawn.jpg: Sound.kicad_pcb drawings.kibot.yaml
	kibot -c ./drawings.kibot.yaml

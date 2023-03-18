TARGET=modelh

all: modelh_gerber.zip assembly/modelh-top-pos.csv assembly/modelh-bom.csv

gerber/%.gbr: $(TARGET).kicad_pcb
	@echo ".kicad_pcb is newer than gerbers. Needs replot."
	@exit 1

gerber/%.drl: $(TARGET).kicad_pcb
	@echo ".kicad_pcb is newer than drill files. Needs replot."
	@exit 1

gerber/modelh-top-pos.csv: $(TARGET).kicad_pcb
	@echo ".kicad_pcb is newer than positions. Needs export."
	@exit 1

modelh_gerber.zip: $(glob gerber/*)
	zip -r $@ gerber/*.drl gerber/*.gbr

modelh.csv: modelh.sch
	@echo "schema is newer than bom. Needs re-export."
	@exit 1

assembly/modelh-bom.csv: modelh.csv
	@mkdir -p assembly/
	cp $< $@

assembly/modelh-top-pos.csv: gerber/modelh-top-pos.csv
	@mkdir -p assembly/
	ruby script/fix_pos.rb $< > $@

clean:
	rm -Rf assembly/
	rm modelh_gerber.zip

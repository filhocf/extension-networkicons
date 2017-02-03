oxtName = NetworkIconsEquipments
oxtVersion = $(shell grep "<version " description.xml.lo_version | cut -f 2 -d \")
files = $(wildcard description.xml gallery/* license/* META-INF/* Paths.xcu pkg-desc/* Release-notes/* template/* networkicons-equipment.png)

all: libreoffice openoffice

openoffice:
	ln -fs description.xml.oo_version description.xml
	zip ../builds/$(oxtName)_$(oxtVersion)-oo.oxt $(files)

libreoffice:
	ln -fs description.xml.lo_version description.xml
	zip ../builds/$(oxtName)_$(oxtVersion)-lo.oxt $(files)

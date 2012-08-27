include /usr/local/share/luggage/luggage.make

PACKAGE_VERSION=16
PACKAGE_MAJOR_VERSION=16
PACKAGE_MINOR_VERSION=0

TITLE=Maple
REVERSE_DOMAIN=edu.rit
PAYLOAD=\
	pack-rit-background \
	pack-from-applications-"Maple\\ 16" \
	pack-Library-Frameworks-Mapleframework

l_Library_Frameworks: l_Library
	@sudo mkdir -p ${WORK_D}/Library/Frameworks
	@sudo chown root:admin ${WORK_D}/Library/Frameworks
	@sudo chmod 775 ${WORK_D}/Library/Frameworks

l_Library_Frameworks_Mapleframework: l_Library_Frameworks
	@sudo mkdir -p ${WORK_D}/Library/Frameworks/Maple.framework
	@sudo chown root:admin ${WORK_D}/Library/Frameworks/Maple.framework
	@sudo chmod 775 ${WORK_D}/Library/Frameworks/Maple.framework

pack-Library-Frameworks-Mapleframework: l_Library_Frameworks_Mapleframework
	@sudo ${DITTO} /Library/Frameworks/Maple.framework ${WORK_D}/Library/Frameworks/Maple.framework

pack-rit-background: resourcedir
	@sudo ${INSTALL} -m 755 /usr/local/share/luggage/background ${RESOURCE_D}


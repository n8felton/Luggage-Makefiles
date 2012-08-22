include /usr/local/share/luggage/luggage.make

PACKAGE_VERSION=11.4.402.265
PACKAGE_MAJOR_VERSION=11
PACKAGE_MINOR_VERSION=4

TITLE=Adobe_Flash_Player
REVERSE_DOMAIN=edu.rit
PAYLOAD=\
	pack-rit-background \
	pack-adobe-flash-"Install\\ Adobe\\ Flash\\ Player.app" \
	pack-script-postflight
	
pack-rit-background: resourcedir
	@sudo ${INSTALL} -m 755 /usr/local/share/luggage/background ${RESOURCE_D}
	
pack-adobe-flash-%: % resourcedir
	@sudo ${DITTO} "${<}" ${RESOURCE_D}/"${<}"
	@sudo defaults write ${RESOURCE_D}/"${<}"/Contents/Info LSUIElement -int 1
	@sudo chmod a+r ${RESOURCE_D}/"${<}"/Contents/Info.plist

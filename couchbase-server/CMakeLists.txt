# Determine license file name
if (BUILD_ENTERPRISE)
  SET (license license/ee-license.txt)
  SET (license_html license/ee-license.html)
ELSE (BUILD_ENTERPRISE)
  SET (license license/ce-license.txt)
  SET (license_html license/ce-license.html)
ENDIF (BUILD_ENTERPRISE)

# Install license and README files
INSTALL (FILES ${license} RENAME "LICENSE.txt" DESTINATION .)
INSTALL (FILES readme/README.txt DESTINATION .)

IF (APPLE)
  INSTALL (FILES ${license_html} RENAME "Credits.html" DESTINATION .)
ENDIF (APPLE)

# Determine license file name
if (BUILD_ENTERPRISE)
  SET (license license/ee-license.txt)
  SET (license_nocr license/ee-license-no-newlines.txt)
  SET (ns_server_license EE_subscription_license_agreement.txt)
  SET (license_html license/ee-license.html)
ELSE (BUILD_ENTERPRISE)
  SET (license license/ce-license.txt)
  SET (license_nocr license/ce-license-no-newlines.txt)
  SET (ns_server_license CE_license_agreement.txt)
  SET (license_html license/ce-license.html)
ENDIF (BUILD_ENTERPRISE)

# Install license and README files
INSTALL (FILES ${license} RENAME "LICENSE.txt" DESTINATION .)
INSTALL (FILES ${license_nocr} RENAME "${ns_server_license}" DESTINATION lib/ns_server/erlang/lib/ns_server/priv/public/ui)
INSTALL (FILES readme/README.txt DESTINATION .)

IF (APPLE)
  INSTALL (FILES ${license_html} RENAME "Credits.html" DESTINATION .)
ENDIF (APPLE)

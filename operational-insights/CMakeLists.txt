# Determine license file name
SET (license ../couchbase-server/license/ee-license.txt)
SET (license_nocr ../couchbase-server/license/ee-license-no-newlines.txt)
SET (ns_server_license EE_subscription_license_agreement.txt)
SET (license_html ../couchbase-server/license/ee-license.html)

# Install license and README files
INSTALL (FILES ${license} RENAME "LICENSE.txt" DESTINATION .)
INSTALL (FILES ${license_nocr} RENAME "${ns_server_license}" DESTINATION lib/ns_server/erlang/lib/ns_server/priv/public/ui)
INSTALL (FILES readme/README.txt DESTINATION .)

IF (APPLE)
  INSTALL (FILES ${license_html} RENAME "Credits.html" DESTINATION .)
ENDIF (APPLE)

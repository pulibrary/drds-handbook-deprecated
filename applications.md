# DRDS Applications

[Architecture diagram](https://docs.google.com/drawings/d/1qqHoceL4nahv8wmhK_QltL8f1StdBJ5GYFpIa6JQ3PA/edit)

## in Production

* Bibdata, aka Marc Liberation
  * Github repository: https://github.com/pulibrary/marc_liberation
  * [Orangelight / Marc Liberation Zenhub board](https://app.zenhub.com/workspaces/orangelightmarcliberation-571691cab409d8d821b873be/board?repos=21954918)
  * Tech lead: [Christina](https://github.com/christinach)
  * Technical slack channel: #orangelight
  * User-centered slack channel: #catalog
* Cicognara-Rails - Blacklight and TEI/MARC app for a multi-institution project to virtually reconstruct a famous art history library
  * https://www.cicognara.org/, https://cicognara-staging.princeton.edu
  * Github repository: https://github.com/pulibrary/cicognara-rails
  * MARC/TEI data reposiory: [https://github.com/pulibrary/cicognara-catalogo]
  * [Cicognara Zenhub board](https://app.zenhub.com/workspaces/cicognara-5cf11cb3689f9c7a4ead9571/board?repos=57136753)
  * Tech lead: [Esmé](https://github.com/escowles), transfer to [Trey](https://github.com/tpendragon)
  * Technical slack channel: #cicognara
  * User-centered slack channel: #digital_library
* DPUL, aka Pomegranate - Spotlight exhibits for showcasing Figgy content
  * https://dpul.princeton.edu/, https://dpul-staging.princeton.edu/
  * Github repository: https://github.com/pulibrary/pomegranate
  * [DPUL Zenhub board](https://app.zenhub.com/workspaces/dpul-5cc9dbb2262a972347170639/board?repos=49439415&showEstimates=false&showReleases=false)
  * Tech lead: [Anna](https://github.com/hackmastera)
  * Product owner: [Kim](https://github.com/kelea99)
  * Technical slack channel: #figgy
  * User-centered slack channel: #digital_library
* Figgy - Samvera/Valkyrie app for managing ingest and workflow, generating IIIF
  * figgy.princeton.edu, figgy-staging.princeton.edu
  manifests for other apps
  * Github repository: https://github.com/pulibrary/figgy
  * [Figgy Zenhub board](https://app.zenhub.com/workspaces/figgystudio-5c06d2e24b5806bc2bfa890b/board)
  * Tech lead: [Trey](https://github.com/tpendragon)
  * Product owner: [Kim](https://github.com/kelea99)
  * Technical slack channel: #figgy
  * User-centered slack channel: #digital_library
* LAE-Blacklight - Latin American Ephemera frontend
  * https://lae.princeton.edu
  * Github repository: https://github.com/pulibrary/lae-blacklight
  * Tech lead: [Trey](https://github.com/tpendragon), transfer to [Eliot](https://github.com/eliotjordan)
  * Technical slack channel: #figgy
  * User-centered slack channel: #digital_library
* Maps Portal, aka PULMap - GeoBlacklight app for maps and geo data discovery and access
  * https://maps.princeton.edu
  * Github repository: https://github.com/pulibrary/pulmap
  * [Pulmap Zenhub board](https://app.zenhub.com/workspaces/pulmap-5cf5538c08e7e9307cd79c45/board?repos=26446857)
  * Tech lead: [Eliot](https://github.com/eliotjordan)
* Orangelight - our blacklight catalog (aka The Catalog)
  * https://catalog.princeton.edu/, https://catalog-staging.princeton.edu/
  * Github repository: https://github.com/pulibrary/orangelight
  * [Orangelight / Marc Liberation Zenhub board](https://app.zenhub.com/workspaces/orangelightmarcliberation-571691cab409d8d821b873be/board?repos=21954918)
  * Tech lead: [Nikitas](https://github.com/tampakis)
  * Technical slack channel: #orangelight
  * User-centered slack channel: #catalog
* Orangetheses - interfacing between DSpace and Orangelight
  * Github repository: https://github.com/pulibrary/orangetheses
  * Tech lead: [James](https://github.com/jrgriffiniii)
  * Technical slack channel: #orangelight
  * User-centered slack channel: #catalog
* PULBot/Heaven - Slack bot for deployments
  * Github repository: https://github.com/pulibrary/pulbot
  * Github repository: https://github.com/pulibrary/heaven
  * Tech lead: [Trey](https://github.com/tpendragon), transfer to [Christina](https://github.com/christinach)
  * Slack channels: #robots, #devs
* PUL-Solr - Central repository of solr configs for our apps
  * Github repository: https://github.com/pulibrary/pul_solr
  * Tech lead: [Anna](https://github.com/hackmastera)
  * Slack channel: #solr
* DSpace
  * Github repository: https://github.com/pulibrary/dspace
  * There are many repos built off DSpace to aid with statistics reporting, collection and user management, bulk ingest, and regulatory compliance. [Read more here.](https://dspace-development.readthedocs.io/en/latest/index.html)
  * Tech lead: [James](https://github.com/jrgriffiniii)
  * Technical slack channel: #operations
  * User-centered slack channel: #dspace

# In Development

* PULFALight - Local instance of arclight
  * Github repository: https://github.com/pulibrary/pulfalight
  * [PULFALight Zenhub board](https://app.zenhub.com/workspaces/pulfalight-5da4b7d9f037f100019dba23/board?repos=157741631)
  * Tech lead: [James](https://github.com/jrgriffiniii)
  * Product owners: [Faith](https://github.com/faithc) and [Amanda](https://github.com/apferrar)
  * Slack channel: #pulfalight

## Other Applications

Many applications led / managed by other teams are relevant to our work.

* [Princeton Ansible](https://github.com/pulibrary/princeton_ansible) -
  playbooks for all of our server provisioning
* [Voyager helpers](https://github.com/pulibrary/voyager_helpers) provides data used by bibdata
* [Requests](https://github.com/pulibrary/requests) - an engine used in Orangelight for managing various services patrons can use to request materials. In the process of being refactored into orangelight.
* [Valkyrie](https://github.com/samvera-labs/valkyrie) - samvera persistence
  layer on which Figgy is built
* [PUDL](http://pudl.princeton.edu/) - the precursor to dpul; about half of
  this content has bibliographic metadata and has been migrated to Figgy. The other half has
  local-only metadata and migration is still in progress
    * METS-creation logic at https://github.com/pulibrary/pudl-mets and
  https://github.com/pulibrary/pudl_mets_compiler
* SCSB - Shared Collections Service Bus. middle application that provides an API to pull the [ReCAP](https://recap.princeton.edu/) shared multi-institution collection into our catalog. NYPL, Columbia, and Harvard. Also provides APIs to request and check the status of our own and Partner ReCAP items.
  * [General Technical Docs](https://htcrecap.atlassian.net/wiki/spaces/RTG/pages/2129960/Technical+Documentation)
  * [Documentation for RESTful API](https://htcrecap.atlassian.net/wiki/spaces/RTG/pages/2129950/RESTful+Services)
  * [SCSB related code](https://github.com/ResearchCollectionsAndPreservation ) is open source
  * In Marc Liberation: we use https://htcrecap.atlassian.net/wiki/spaces/RTG/pages/23232564/Item+Availability+Status
  * In the Requests gem we use https://htcrecap.atlassian.net/wiki/spaces/RTG/pages/25438542/Request+Item
  * [Staff Backend](https://scsb.recaplib.org/)
  * [Staff Backend UAT](https://uat-recap.htcinc.com/)
  * [UAT API](https://uat-recap.htcinc.com:9093/swagger-ui.html#/)
  * [Prod API](https://scsb.recaplib.org:9093/swagger-ui.html#/)

# Related services
* [CAS](https://www.princeton.edu/cas) - authentication
* [GeoServer](http://geoserver.org/) - Geo data server
* [Cantaloupe](https://github.com/medusa-project/cantaloupe) - IIIF image API server
* Isilon - storage
* Nginx+ - load balancer
* [Kakadu](http://kakadusoftware.com/downloads/) - for generating JP2s
* [Tesseract](https://github.com/tesseract-ocr/tesseract) - OCR software
* Characterization tools
  * [FITS](https://projects.iq.harvard.edu/fits) - default Samvera/Hyrax characterization
  * [Tika](https://tika.apache.org/) - (part of FITS) Apache text analysis/parsing framework
  * [JHove](https://github.com/openpreserve/jhove) - (part of FITS) good TIFF validation

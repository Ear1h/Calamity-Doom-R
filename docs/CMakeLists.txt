set(CALAMITYDOOM_DOCS
    boom.txt
    boomdeh.txt
    boomref.txt
    mbf.txt
    mbfedit.txt
    mbffaq.txt
    nughud.lmp # [Nugget]
    nughud.md # [Nugget]
    options.txt)

if(WIN32)
    install(FILES ${CALAMITYDOOM_DOCS} DESTINATION docs)
else()
    install(FILES ${CALAMITYDOOM_DOCS} DESTINATION "share/doc/${PROJECT_SHORTNAME}")
endif()

include_directories( $ENV{IFDHC_FQ_DIR}/inc )
include_directories( ${CMAKE_CURRENT_SOURCE_DIR} )
art_make( BASENAME_ONLY
          MODULE_LIBRARIES dune_EventGenerator_ProtoDUNEbeamDataProducts
                        larcoreobj_SummaryData
                        larcorealg_Geometry
                        larcore_Geometry_Geometry_service
                        nurandom_RandomUtils_NuRandomService_service
                        larsim_Simulation lardataobj_Simulation
			lardataobj_RecoBase
                        nusimdata_SimulationBase
                        ${ART_FRAMEWORK_CORE}
                        ${ART_FRAMEWORK_PRINCIPAL}
                        ${ART_FRAMEWORK_SERVICES_REGISTRY}
                        ${ART_FRAMEWORK_SERVICES_OPTIONAL}
                        ${ART_FRAMEWORK_SERVICES_OPTIONAL_TFILESERVICE_SERVICE}
                        ${ART_FRAMEWORK_SERVICES_OPTIONAL_RANDOMNUMBERGENERATOR_SERVICE}
                        art_Persistency_Common
                        art_Persistency_Provenance
                        art_Utilities canvas
                        ${MF_MESSAGELOGGER}
                        hep_concurrency
                        ${FHICLCPP}
                        cetlib cetlib_except
                        ${CLHEP}
                        ${ROOT_BASIC_LIB_LIST}
                        ${SQLITE3}
                        ${ROOT_EG}
                        ${IFDH}
			ProtoDUNEDataUtils
                        ProtoDUNEUtilities
                        ${ART_ROOT_IO_TFILE_SUPPORT} ${ROOT_CORE}
                        ${ART_ROOT_IO_TFILESERVICE_SERVICE}
 )


install_headers()
install_fhicl()
install_source()

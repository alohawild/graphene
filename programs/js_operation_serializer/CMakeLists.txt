add_executable( js_operation_serializer main.cpp )
if( UNIX AND NOT APPLE )
  set(rt_library rt )
endif()

target_link_libraries( js_operation_serializer
                       PRIVATE graphene_app graphene_net graphene_chain graphene_utilities graphene_wallet fc ${CMAKE_DL_LIBS} ${PLATFORM_SPECIFIC_LIBS} )

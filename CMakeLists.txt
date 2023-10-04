cmake_minimum_required(VERSION 3.12)

SET(PXR_PATH "" CACHE STRING "Path to USD install")
SET(PYTHON_PATH "" CACHE STRING "Path to Python install")

project(mpcdiFileFormat)

add_library(mpcdiFileFormat
  MODULE
  api.h 
  iMpcdiDataProvider.cpp iMpcdiDataProvider.h 
  mpcdiData.cpp 
  mpcdiDataProviderFactory.cpp mpcdiDataProviderFactory.h 
  mpcdiFileFormat.cpp 
  mpcdiPluginManager.cpp 
  tinyxml2.cpp tinyxml2.h 
  plugInfo.json

  mpcdiPluginManager.h 
  mpcdiFileFormat.h 
)

target_link_libraries(mpcdiFileFormat
    ${PXR_PATH}/lib/tbb_debug.lib 
    ${PXR_PATH}/lib/tbb.lib 
    ${PXR_PATH}/lib/usd_plug.lib 
    ${PXR_PATH}/lib/usd_usdGeom.lib 
    ${PXR_PATH}/lib/usd_usdLux.lib 
    ${PXR_PATH}/lib/usd_usd.lib 
    ${PXR_PATH}/lib/usd_arch.lib 
    ${PXR_PATH}/lib/usd_tf.lib 
    ${PXR_PATH}/lib/usd_vt.lib 
    ${PXR_PATH}/lib/usd_sdf.lib 
    ${PXR_PATH}/lib/usd_js.lib 
    ${PXR_PATH}/lib/usd_pcp.lib 
    ${PXR_PATH}/lib/usd_gf.lib 
)

target_include_directories(mpcdiFileFormat
    PRIVATE
    ${PXR_PATH}/include
	${PYTHON_PATH}/include
    ${PXR_PATH}/include/boost-1_78
)
set_target_properties(mpcdiFileFormat
    PROPERTIES
    PREFIX ""
)

TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = autoIOC
# autoIOC.dbd will be created and installed
DBD += autoIOC.dbd

# autoIOC.dbd will be made up from these files:
autoIOC_DBD += base.dbd

# Include dbd files from all support applications:
autoIOC_DBD += asSupport.dbd

# Add all the support libraries needed by this IOC
autoIOC_LIBS += autosave

# autoIOC_registerRecordDeviceDriver.cpp derives from autoIOC.dbd
autoIOC_SRCS += autoIOC_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
autoIOC_SRCS_DEFAULT += autoIOCMain.cpp
autoIOC_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#autoIOC_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
autoIOC_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE


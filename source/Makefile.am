##########################################################################
# If not stated otherwise in this file or this component's Licenses.txt
# file the following copyright and licenses apply:
#
# Copyright 2015 RDK Management
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
##########################################################################
AM_CFLAGS = -D_ANSC_LINUX
AM_CFLAGS += -D_ANSC_USER
AM_CFLAGS += -D_ANSC_LITTLE_ENDIAN_
AM_LDFLAGS = -lccsp_common
AM_LDFLAGS += -lsyscfg
AM_LDFLAGS += -lutapi 
AM_LDFLAGS += -lutctx

AM_CPPFLAGS = -Wall -Werror
ACLOCAL_AMFLAGS = -I m4
hardware_platform = i686-linux-gnu
bin_PROGRAMS = PsmSsp
PsmSsp_CPPFLAGS = -I$(top_srcdir)/source/DslhManagementServer -I$(top_srcdir)/../CcspCommonLibrary/source/cosa/package/system/include -I$(top_srcdir)/source/include $(CPPFLAGS)
PsmSsp_CFLAGS = $(SYSTEMD_CFLAGS)
PsmSsp_SOURCES = Ssp/ssp_main.c Ssp/ssp_dbus.c Ssp/ssp_cfmif.c PsmFileLoader/psm_flo_interface.c PsmFileLoader/psm_flo_control.c PsmFileLoader/psm_flo_parse.c PsmFileLoader/psm_flo_operation.c PsmFileLoader/psm_flo_states.c PsmFileLoader/psm_flo_base.c PsmSysRegistry/psm_sysro_states.c PsmSysRegistry/psm_sysro_interface.c PsmSysRegistry/psm_sysro_storage.c PsmSysRegistry/psm_sysro_sysramif.c PsmSysRegistry/psm_sysro_base.c PsmSysRegistry/psm_sysro_cfmif.c PsmSysRegistry/psm_sysro_operation.c PsmSysRegistry/psm_sysro_control.c Ssp/psm_hal_apis.c

PsmSsp_LDFLAGS =  -lccsp_common $(SYSTEMD_LDFLAGS) -lsyscfg -lutapi -lutctx

#
# Copyright 2008 Ettus Research LLC
#

##################################################
# Project Setup
##################################################
TOP_MODULE = u2_rev3
BUILD_DIR = $(abspath build)

##################################################
# Include other makefiles
##################################################

include ../Makefile.common
include ../../fifo/Makefile.srcs
include ../../control_lib/Makefile.srcs
include ../../sdr_lib/Makefile.srcs
include ../../serdes/Makefile.srcs
include ../../simple_gemac/Makefile.srcs
include ../../timing/Makefile.srcs
include ../../opencores/Makefile.srcs
include ../../vrt/Makefile.srcs
include ../../udp/Makefile.srcs
include ../../coregen/Makefile.srcs
include ../../extramfifo/Makefile.srcs


##################################################
# Project Properties
##################################################
PROJECT_PROPERTIES = \
family Spartan3 \
device xc3s2000 \
package fg456 \
speed -5 \
top_level_module_type "HDL" \
synthesis_tool "XST (VHDL/Verilog)" \
simulator "ISE Simulator (VHDL/Verilog)" \
"Preferred Language" "Verilog" \
"Enable Message Filtering" FALSE \
"Display Incremental Messages" FALSE 

##################################################
# Sources
##################################################
TOP_SRCS = \
u2_core.v \
u2_rev3.v \
u2_rev3.ucf

SOURCES = $(abspath $(TOP_SRCS)) $(FIFO_SRCS) \
$(CONTROL_LIB_SRCS) $(SDR_LIB_SRCS) $(SERDES_SRCS) \
$(SIMPLE_GEMAC_SRCS) $(TIMING_SRCS) $(OPENCORES_SRCS) \
$(VRT_SRCS) $(UDP_SRCS) $(COREGEN_SRCS) $(EXTRAM_SRCS)

##################################################
# Process Properties
##################################################
SYNTHESIZE_PROPERTIES = \
"Number of Clock Buffers" 8 \
"Pack I/O Registers into IOBs" Yes \
"Optimization Effort" High \
"Optimize Instantiated Primitives" TRUE \
"Register Balancing" Yes \
"Use Clock Enable" Auto \
"Use Synchronous Reset" Auto \
"Use Synchronous Set" Auto

TRANSLATE_PROPERTIES = \
"Macro Search Path" "$(shell pwd)/../../coregen/"

MAP_PROPERTIES = \
"Generate Detailed MAP Report" TRUE \
"Allow Logic Optimization Across Hierarchy" TRUE \
"Map to Input Functions" 4 \
"Optimization Strategy (Cover Mode)" Speed \
"Pack I/O Registers/Latches into IOBs" "For Inputs and Outputs" \
"Perform Timing-Driven Packing and Placement" TRUE \
"Map Effort Level" High \
"Extra Effort" Normal \
"Combinatorial Logic Optimization" TRUE \
"Register Duplication" TRUE

PLACE_ROUTE_PROPERTIES = \
"Place & Route Effort Level (Overall)" High 

STATIC_TIMING_PROPERTIES = \
"Number of Paths in Error/Verbose Report" 10 \
"Report Type" "Error Report"

GEN_PROG_FILE_PROPERTIES = \
"Configuration Rate" 6 \
"Create Binary Configuration File" TRUE \
"Done (Output Events)" 5 \
"Enable Bitstream Compression" TRUE \
"Enable Outputs (Output Events)" 6 

SIM_MODEL_PROPERTIES = ""

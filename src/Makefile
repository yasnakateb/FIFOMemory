#TOOL INPUT
SRC =Compare_Logic.v Read_Interface.v Fifo_Memory.v Memory_Array.v Write_Interface.v
TESTBENCH = Fifo_Memory_tb.v
TBOUTPUT = Fifo_Memory_tb.vcd

#TOOLS
COMPILER = iverilog
SIMULATOR = vvp
VIEWER = Scansion

#TOOL OPTIONS
COFLAGS = -v -o
SFLAGS = -v

#TOOL OUTPUT
COUTPUT = compiler.out          

###############################################################################

simulate: $(COUTPUT)
	$(SIMULATOR) $(SFLAGS) $(COUTPUT) 

display: 
	open -a $(VIEWER) $(TBOUTPUT) 

$(COUTPUT): $(TESTBENCH) $(SRC)
	$(COMPILER) $(COFLAGS) $(COUTPUT) $(TESTBENCH) $(SRC)
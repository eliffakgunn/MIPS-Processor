# MIPS-Processor

A 32 bit Mips processor that supports lw, sw, j, jal, jr, beq, bne, addn, subn, xorn, andn, orn, ori and lui instructions.
The R-type instructions executes different than the conventional MIPS. This is why they have ‘n’ at the end (representing new).
The new instructions have the same opcode and function fields as the conventional R-type instructions. For instance the opcode and function field of orn is same as or.
But the execution is different.  
  
For instance: addn $rd, $rs, $rt  

RTL Representation:  
$rs <= $rs + $rt  
if($rs + $rt == 0)  
$rd <= 1  
else if($rs + $rt < 0)  
$rd <= 2  
else  
$rd <= 3  

You can check homework file and report for more details and sample input/output.

<table width="100%">
 <tr width="100%">
    <td align="center"><img src="https://www.xilinx.com/content/dam/xilinx/imgs/press/media-kits/corporate/xilinx-logo.png" width="30%"/><h1>2020.1 Vitis™ - Algorithm Acceleration</h1>
    <a href="https://www.xilinx.com/products/design-tools/vitis.html">See Vitis™ Development Environment on xilinx.com</a>
    </td>
 </tr>
</table>

This section is divided in 5 modules (each module has its own readme with step-by-step instructions).
* **Module 1**: Setting up the design and establish a performance **baseline**
  + Understand the OpenCL APIs that help connect host program to the kernel
  + Verify the algorithm results through emulation both at the software level (sw_emu) and the hardware level (hw_emu)
  + Evaluate the performance by visualizing the timeline trace with Vitis Analyzer
* **Module 2**: Apply a first level of optimization with the **PIPELINE** directive to improve throughput
  + Using the module 1 results as a starting point to review the kernel performance in Vitis HLS
  + Run the sw_emu step and use the hw_emu results to quantify the performance improvement 
* **Module 3**: Analyze and solve false dependencies to further improve the kernel
  + Reuse the results from module 2 to study how these dependencies come into play.
  + Apply the **DEPENDENCE** pragma
  + Rerun the kernel and observe the results
* **Module 4**: Merge and flatten critical loop to implement more parallelism
  + Reuse the results from module 3 and flatten a critical loop to gain more parallelism.
  + Rerun and observe the impact on resources, latency and throughput
* **Module 5**: Add the task parallelism pragma to further improve the kernel
  + Reuse the results from module 4 to re-arrange the code to enable the task parallelism optimization pragma called **DATAFLOW**.
  + Evaluate the performance improvement with Vitis Analyzer
  + Create the binary (xclbin) to program the card and measure the actual performance
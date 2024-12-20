# Workflow
*(not yet referenced from elsewhere)*

## Procedure

1. **Rough Sketch Circuit Schematic/Physical PCB**  
   - Identify the functional requirements of the circuit.  
   - Select key components based on requirements.  
   - Place components in logical groups (e.g., power, signal, output).  
   - Create connections between components using the schematic capture tool.  
   - Verify correctness of the schematic (e.g., ensure no missing connections).  
   - Review the schematic against datasheets and application notes.

2. **Draw Planned Outline of PCB**  
   - Define the approximate dimensions of the PCB based on enclosure or space constraints.  
   - Identify areas for specific groups of components (e.g., power section, signal section).  
   - Sketch positions for connectors and mounting holes.  
   - Plan for PCB stackup if using multiple layers (e.g., power planes, signal planes).  
   - Verify that the outline includes proper clearances for manufacturing.

3. **Shuffle Components into Place**  
   - Group components to minimize "rat's nest" connections (e.g., keep related components close).  
   - Place critical components first (e.g., high-speed ICs, power regulators).  
   - Optimize placement for thermal considerations (e.g., heat-generating components).  
   - Check for design rule constraints (e.g., spacing between components).  
   - Reposition connectors for accessibility during assembly or testing.  

4. **Adjust Size/Shape of PCB if Things Don't Fit**  
   - Expand or shrink the outline to accommodate components.  
   - Revisit enclosure constraints to determine allowable size adjustments.  
   - Evaluate alternative placement options before resizing.  
   - Validate that any size changes align with manufacturing capabilities.

5. **Select Different Components if Things Don't Fit**  
   - Identify components with smaller footprints or alternate packages.  
   - Cross-reference substitutions to ensure compatibility (e.g., voltage, current ratings).  
   - Update the schematic with new component selections.  
   - Re-check part availability and lead times for substitutions.

6. **Run Copper Tracks Between Components**  
   - Start with power and ground planes or tracks for low-impedance paths.  
   - Route critical signal paths (e.g., high-frequency, differential pairs) first.  
   - Maintain proper trace widths for current handling.  
   - Follow PCB design rules for clearances and spacing.  
   - Perform a Design Rule Check (DRC) to identify violations.  

7. **Adjust Size/Shape of PCB if Things Don't Fit**  
   - Modify PCB layout to improve trace routing or component placement.  
   - Optimize via placement and layer transitions to reduce complexity.  
   - Verify signal integrity and thermal performance impacts after adjustments.

8. **Select Different Components if Things Don't Fit**  
   - Identify components with more favorable specifications for layout (e.g., lower pin count).  
   - Validate replacement options through simulation or prototyping.  
   - Confirm new components' footprints match available space.  
   - Update the Bill of Materials (BOM) with substitutions. 

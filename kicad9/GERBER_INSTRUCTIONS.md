How to generate Gerbers locally

Open the project in KiCad 9 and follow these steps:
1. Open PCB Editor (Pcbnew)
2. Run 'Design Rules' -> 'Design Rules Checker' and fix any DRC issues
3. Use 'File' -> 'Plot' to generate Gerber files (use RS-274X)
4. Generate drill file (File -> Fabrication Outputs -> Drill Files)
5. Zip the produced gerber files for fabrication

If you want me to generate Gerbers and attach them in the repo, reply “Generate and push Gerbers” and I will run a generation step and add the gerber zip to the branch.

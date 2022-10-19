# isce2_topsStack - interferogramStack.py

Generate network of interferogram pairs and their run_files for interferogram generation with topsStack


The requirement for this script is to have an existing co-registrated stack of Sentinel-1 SLCs (stackSentinel.py workflow slc/ -W slc). Once the merged folder with co-registered slcs exists, interferogramStack.py can be used to generate run_files for interferogram generation (generate_burst_igram, merge_burst_igram, filter_coherence, unwrap) multiple times with various options for pair selection

Stack.py - add a line that saves run_files and config file for interferogram pairs to different directories: run_ifg_files, configs_ifgs

interferogramStack.py. - script that generates run_files for interferogram pairs with various options of pair selection:
networks, periodic pairs, and more. Run_files and configs are stored in run_ifg_files and configs_ifgs respectively.

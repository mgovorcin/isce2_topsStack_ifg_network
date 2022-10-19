# isce2_topsStack - interferogramStack.py

Generate network of interferogram pairs and their run_files for interferogram generation with topsStack


The requirement for this script is to have an existing co-registrated stack of Sentinel-1 SLCs (stackSentinel.py workflow slc/ -W slc). Once the merged folder with co-registered slcs exists, interferogramStack.py can be used to generate run_files for interferogram generation (generate_burst_igram, merge_burst_igram, filter_coherence, unwrap) multiple times with various options for pair selection

Stack.py - add a line that saves run_files and config file for interferogram pairs to different directories: run_ifg_files, configs_ifgs

interferogramStack.py. - script that generates run_files for interferogram pairs with various options of pair selection:
networks, periodic pairs, and more. Run_files and configs are stored in run_ifg_files and configs_ifgs respectively.

        Features:  
             - _networks_ - **sequential** (with number of connections)
                                   Example: sequential w 1 connection

<img width="648" alt="Screen Shot 2022-07-25 at 11 09 16 AM" src="https://user-images.githubusercontent.com/26017189/180845223-697ecb5a-06ba-49ba-86e2-d21b75fd1481.png">

                                   sequential w 4 connection
<img width="659" alt="Screen Shot 2022-07-25 at 11 10 23 AM" src="https://user-images.githubusercontent.com/26017189/180845402-e9127f3f-b2a8-4b12-aaf3-04001c5c62da.png">

             -  **delaunay**, 
<img width="686" alt="Screen Shot 2022-07-25 at 11 12 08 AM" src="https://user-images.githubusercontent.com/26017189/180845568-2c7f142e-57d1-469c-ad7e-24750755c9f7.png">

             - **single_reference**
<img width="676" alt="Screen Shot 2022-07-25 at 11 12 42 AM" src="https://user-images.githubusercontent.com/26017189/180845671-1ad5df33-cf0d-4510-8743-544dec0f15ae.png">

             - **full network**
<img width="689" alt="Screen Shot 2022-07-25 at 11 12 52 AM" src="https://user-images.githubusercontent.com/26017189/180845807-7d22fae7-1918-42f6-8ef4-e6ffc8ce9b20.png">

             - _periodic_pairs_ -  include periodic pairs such as semi-annual and annual pairs
                             - Example: sequential w 1 connection and 18d periodic pairs
<img width="685" alt="Screen Shot 2022-07-25 at 11 15 08 AM" src="https://user-images.githubusercontent.com/26017189/180846126-4a80e9b0-27d4-4ac2-baeb-ea6b4eaabff7.png">

             - _update the current network_ with more interferograms for a specific date period ( use start_date and end_date)

             - _limit_ selection of _pairs_ based on maximum perpendicular and temporal baseline (use max_bperp and max_btemp)
             - Script detects and skips the existing interferograms in the merged/interferograms directory (_update mode_)
 <img width="695" alt="Screen Shot 2022-07-25 at 11 16 45 AM" src="https://user-images.githubusercontent.com/26017189/180846272-bef0376a-0a47-47d2-8536-7e650823e7f3.png">


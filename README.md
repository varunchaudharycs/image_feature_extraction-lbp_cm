# phase1_cm.py, phase1_lbp.py 

This python script performs the following given tasks using **color moments** and/or **local binary patterns**:

  - TASK 1: Implement a program which, given an image ID and one of the following models, extracts and prints (in a human readable form) the corresponding feature descriptors
  - TASK 2: Implement a program which, given a folder with images, extracts and stores feature descriptors for all the images in the folder.
  - TASK 3: Implement a program which, given an image ID, a model, and a value “k”, returns and visualizes the most
similar k images based on the corresponding visual descriptors. For each match, also list the overall matching score.

### Packages

Packages for implementation:

* [Anaconda] - Anaconda is a free and open-source distribution of Python programming language that aims to simplify package management and deployment(Python 3.6 version). {https://www.anaconda.com/distribution/}
* [OpenCV] - pre-built OpenCV packages for Python. {https://pypi.org/project/opencv-python/}


### Installation

Requires opencv v4.1 to run.

Install the package

```sh
$ conda install -c conda-forge opencv=4.1.0
```

#### Execution
For running script(while in the same directory as the program):

```sh
$ python phase1_cm.py
$ python phase1_lbp.py
```
### Task Implementation
Both scripts perform the given tasks(1, 2 and 3) as user-input options

For Task 1(choose option 1):

```sh
Enter the output folder to store all results: /home/varun/Desktop/MWDB/Project/output

Enter the task option to execute(or 9 to quit) 
1. Task 1 (extract and print feature descriptors for given image ID) 
2. Task 2 (extract and stores feature descriptors for all images in given folder) 
3. Task 3 (pre-requisite: Task 2; given an image ID- finds 'k' most similar images) 
9. Quit
Option? 1
TASK 1:

Enter the dataset folder path: /home/varun/Desktop/MWDB/Project/input
Enter the image id: 0008110
Output saved in file - 
 /home/varun/Desktop/MWDB/Project/output/0008110_cm_image_09152019_192215.csv
Color moments of image Id - 0008110: 
[[128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [125.43230000000001, 128.4571, 253.34040000000002, 4.018782988666824, 0.7748287488214107, 2.827530342895455, -0.527143168237689, -0.12106791046178729, 0.07879574737396831], [121.75200000000001, 128.4011, 117.6726, 5.104693526549703, 1.5794995378274808, 101.26665595960006, -0.5100010190023557, -0.31358015360939434, 0.2360788172208404], [128.5182, 126.4706, 30.9205, 4.728918349897873, 2.8593243327750355, 16.419962842527994, 3.7368105980705324, -2.4490557080611914, 2.4600326684892666], [126.9285, 127.7761, 25.933500000000002, 0.4898854457924553, 0.42798223094098015, 0.26282646365978024, -1.1203450692570736, -0.5424542570165313, 0.5762840716774176], [127.1152, 127.8272, 25.9872, 0.3192631516460772, 0.3780742784160974, 0.12584180545405116, -0.4954049726804607, -1.3113084015427998, 1.2045230748430955], [126.60560000000001, 128.3719, 118.01660000000001, 1.7468396148470107, 0.937651529086503, 108.05799148808939, -0.038184754113318856, -0.30205259463146994, -0.4102392116398214], [127.89920000000001, 128.00140000000002, 254.9658, 0.47899828809574113, 0.03739037304273316, 0.2205229239888872, -0.3444907126973684, 0.12953821759674475, -0.28713617182293333], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [126.27680000000001, 128.2965, 254.0386, 3.060454502193924, 0.6089234352513224, 1.8488131436145516, -0.3363091610144308, 0.3024442068761328, -0.17386724487831737], [126.8846, 124.1508, 187.7263, 13.21088501350306, 7.83717164288243, 71.69527591347983, -1.0194215615854045, -0.254761014423004, 0.0938863378381979], [149.9127, 111.5476, 175.12220000000002, 3.9245227365888806, 2.7203187754376885, 17.615784602452205, -2.6981282765499035, 0.1814382506791811, -0.29620799344945686], [147.9422, 114.8906, 158.1706, 9.629520193654429, 6.123939225694363, 63.93437178576166, -1.4644544926646823, 0.9526533407880283, -1.1439415201876295], [140.8929, 120.2908, 122.96170000000001, 11.529849504221708, 6.215950077019584, 85.5283837863782, -0.1909594618688955, 0.24181584513468957, -0.28895666765107353], [130.75, 126.3722, 181.4694, 8.09499227918107, 4.416386210466536, 99.0948316696688, -0.7567576381440296, 0.12016941457698185, 0.009021470675230946], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [127.1372, 128.0997, 254.5592, 1.6118238613444196, 0.31457894080722226, 0.9608825942852427, -0.17522287481345286, 0.07387772555641106, -0.03782023026888746], [140.73760000000001, 116.84020000000001, 206.20520000000002, 14.536655263161354, 7.77798585496257, 28.51412444666668, -0.07166367147360114, 0.0052444375099236756, 0.03264337081073109], [158.80200000000002, 106.0446, 169.6351, 4.365890058166019, 2.736824956039415, 13.110100990839271, -0.46675553735908976, -0.006341414888814609, -0.06084643325157931], [157.8143, 106.7617, 171.3656, 4.840435466980267, 3.4343140668844603, 17.614344627036292, -0.2942461395346401, -0.158143005246732, 0.29637126948592135], [155.4847, 114.68, 203.3206, 4.197566665343298, 1.9335976830765942, 9.498874440690354, -0.16987330223329222, 0.017010971597056678, 0.06503201973934364], [144.1596, 119.9328, 235.4263, 11.789661905245499, 5.712572464310635, 14.055695226846684, -0.281636359356246, -0.2647603811728011, 0.23813628227379194], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [127.64630000000001, 127.7915, 253.9436, 1.6851695196619945, 1.2745304037177398, 5.643812456132886, -0.5923594472483904, -0.40753053733296296, -0.19106187305214958], [152.2696, 112.4522, 199.6617, 8.638212537325217, 3.829897539099278, 12.99674009550104, 0.06110518585271573, 0.10020447887779661, 0.26488354369118383], [162.13750000000002, 104.9885, 177.48860000000002, 2.875064129718794, 2.7388624919847673, 13.343712753203183, 0.023596364116312357, 0.22080381692155676, 0.3807373780513853], [162.30440000000002, 104.7427, 156.119, 4.956787330519221, 1.9988238316569624, 13.874503198313102, -0.19018704437959236, 0.29571527544368714, 0.102220419695764], [161.6688, 109.49260000000001, 187.5166, 3.1177406178193543, 3.2950485944820014, 13.196352694589255, -0.20768644400461234, -0.3032984783056858, 0.380011207392729], [157.4691, 115.1935, 217.43820000000002, 7.665183963219827, 2.7610609826658923, 12.531798783893354, 0.001976242562968595, -0.03613348372441249, -0.11451304060954497], [130.3272, 126.95270000000001, 252.1293, 7.9737908274545894, 3.4991802911537753, 9.456224484962394, -0.18300305912737194, -0.16166735506744956, 0.02293801679878344], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [130.222, 125.8354, 245.615, 7.118575419281467, 4.878453324569088, 21.65953773744953, -0.08649348557349161, -0.03919228224986013, -0.11376382034841011], [161.66230000000002, 111.01830000000001, 203.77540000000002, 4.5533129378504205, 1.7693968209527817, 10.718999712659675, 0.311042354595404, -0.14791477854042173, -0.21627292712195906], [162.6019, 108.3645, 200.4051, 3.0931563798169845, 3.3780526564870725, 13.644368581579737, -0.06893932935309015, -0.329937499497359, -0.20610501163729322], [165.44330000000002, 104.72250000000001, 172.1339, 4.017136431588564, 3.1403333819833805, 21.32761990448062, 0.3233793080084199, 0.7236885639073134, 0.07376329682279008], [170.27450000000002, 107.3909, 144.918, 6.231897764725802, 4.317024112742554, 33.88175727437996, -0.05981347499930717, 0.08496163974419918, 0.13035913690940026], [168.3094, 110.1547, 180.8316, 6.5182261114507725, 4.094870927147562, 35.46723334910685, 0.06346000477144036, 0.16427289734854875, -0.004144533072573557], [130.8491, 126.7813, 251.43210000000002, 9.429121337113147, 3.998333441572836, 11.337291986624981, -0.15762734554353464, -0.2331746297831549, -0.021661542767944544], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [130.5616, 125.8649, 246.7294, 7.425254570720341, 5.328906828796925, 21.50005989852136, -0.17262066933291464, -0.13603123557962118, -0.2638456272902213], [162.92270000000002, 108.7904, 195.92700000000002, 6.172335434014787, 3.9899959699226915, 18.754558672493456, -0.4192821015309407, -0.6273643929668699, -0.0026158310322171715], [161.2927, 112.1383, 215.5903, 5.424170601115149, 3.296418224376345, 7.480618016580722, -1.2475286384784459, -0.9733145872143136, 0.7479201515262974], [165.9949, 109.71050000000001, 205.8691, 4.948805309365057, 4.102839230337765, 11.83775169489553, -0.9195565148211282, -0.6112123159518197, -0.033555921932321334], [166.6926, 111.68050000000001, 161.3761, 5.596651252311617, 4.119177071940384, 47.61104334910125, -0.7909105299389789, -0.1454358391496125, 0.000772711600681278], [164.24360000000001, 113.313, 190.0705, 12.272043800443221, 5.896628782618118, 35.94112310084364, -0.594062743747625, -0.6438361737326683, 0.2902720436106536], [127.9805, 127.992, 254.96370000000002, 0.3700266882252199, 0.1460684770913696, 0.2217708501914728, -0.08711772374568261, -0.09059771202590186, -0.10802644642583879], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.1014, 127.6483, 254.20510000000002, 1.592833337168748, 1.476891028478194, 5.1115001702034695, -0.2511595263268904, -0.20315626118420044, 0.06224112965234254], [159.31390000000002, 111.6554, 194.41680000000002, 8.929387817202128, 4.384432784295036, 38.41978237522943, -0.696899631727771, -0.6927744985664704, -0.059128556573857786], [167.1561, 109.3819, 189.0343, 5.611660430745645, 4.639962541874543, 35.979826618676285, -0.20186458515939315, 0.013004840960067984, -0.2929301584207906], [168.8041, 110.9012, 191.30800000000002, 6.07820065397639, 3.8033719986350305, 34.121508407454556, -0.08715712356268093, -0.16062648040003036, -0.7183959019745828], [168.13160000000002, 113.29440000000001, 183.51950000000002, 7.178222721537226, 4.256656979367394, 37.71373781196967, 0.19790996898269372, -0.20152672730514742, -0.3880731311698109], [167.83700000000002, 112.2928, 176.9504, 15.627687960795651, 7.241178644392211, 41.16694717658815, 0.3510015993902211, 0.45347260653525734, -0.7448109542991186], [128.0004, 127.97940000000001, 254.9456, 0.34871168606783426, 0.17825722986223874, 0.23460741676210548, 0.06462468755476652, -0.07892687591849507, -0.07980594595425246], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [127.9796, 127.94210000000001, 254.9324, 0.20195009284168894, 0.37622810899449255, 0.3883686908125002, -0.3991649788923907, -0.6519660933788431, -0.18883676926289522], [157.03740000000002, 111.8264, 193.6489, 13.777626836287812, 6.661566110157588, 38.49089540125045, -0.38779102687929345, -0.2223518526869687, -0.26985637617078123], [165.16930000000002, 111.2217, 174.67260000000002, 5.659508592624817, 4.5423506150452875, 42.73797853478798, -0.5363697757434579, -0.13969578971678723, 0.027864622804964944], [170.16420000000002, 111.2061, 173.21630000000002, 4.868679324004859, 3.7542539591775026, 34.28341748294642, -0.2879667842400718, -0.42031731275138945, -0.2681331473272769], [164.6593, 115.9115, 206.5256, 12.91613036129628, 5.97287767746844, 19.47554221684231, -0.40196140016846016, -0.6397757665056802, -0.0796369411610495], [129.3106, 127.38990000000001, 251.8958, 6.981627864617396, 3.1632385287862377, 16.400961629123945, -4.769177789057554, -3.27753702007293, 2.4697187644724288], [128.0017, 128.0, 254.9983, 0.04119599496625511, 0.0, 0.04119599501040963, -0.2592084344631631, 0.0, 0.2592084344631631], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 127.9872, 255.0, 0.0, 0.11241067564783008, 0.0, 0.0, -0.03086974532565347, 0.0], [150.76090000000002, 116.003, 211.3702, 19.59341550598051, 9.045440343067998, 36.879446199204175, -0.5994794791876686, -0.2947739347661949, -0.16489407874747447], [167.3947, 111.3417, 154.6896, 5.088271996464203, 3.9231289948202575, 44.313686958320226, -0.5588898114706911, -0.10125514144860569, -0.18708699477255397], [169.41060000000002, 110.1323, 149.31310000000002, 4.767746599809619, 3.2688830982462536, 32.55772824369041, 0.049071618561834014, -0.3667991009142062, -0.06529353502152874], [164.6125, 113.2669, 197.39600000000002, 18.961997356554903, 8.21609788098947, 32.010707333640674, -0.5232801817866372, -0.34925932713329544, 0.1179650578274627], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.51250000000002, 126.98410000000001, 251.20790000000002, 5.010174023923238, 3.261755231466281, 15.387594925458242, -2.1433788189569727, -1.391206033538166, 1.3092075013676265], [157.4137, 115.7022, 157.41, 19.36524599146621, 6.398805760452474, 52.42426251269539, -0.2727301698676238, -0.3923888907240641, 0.17585583720476808], [168.2896, 111.25290000000001, 149.55450000000002, 6.803420598493081, 3.757943798142561, 39.76817106367845, -0.20158531693299828, -0.0694784979874321, -0.0343742222727532], [161.9717, 116.3144, 193.48350000000002, 22.68998675870046, 8.157619299771158, 43.99779003256863, -0.36070281369359986, -0.4662986044417452, -0.0271463023606025], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0017, 127.96000000000001, 254.9777, 0.06997935410145231, 0.2712931993244851, 0.22136555739825844, -0.33998304749287467, -0.4538560852405923, 0.19627413844899536], [136.1465, 124.2004, 227.984, 15.933808011583448, 6.951779616760042, 51.475139086747475, -1.6542191651713043, -1.363206841463216, 0.33165399975644466], [156.4883, 115.5004, 186.71, 19.147231212632192, 8.435863905967198, 46.99101722669986, 1.04469959434854, 1.3137175613303602, -1.204163214422472], [138.5608, 123.56240000000001, 232.0154, 19.450627325616026, 8.05365173322004, 42.850229437425405, -0.46831581313188575, -0.46536944773736755, 0.4778618237812613], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0027, 127.9876, 254.9829, 0.18301013633445418, 0.1644574109012582, 0.1463133281704306, -3.524799668292289, -1.9342425553727527, 0.5976244688783318], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0], [128.0, 128.0, 255.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0]]

```
For Task 2(choose option 2):

```sh
Enter the task option to execute(or 9 to quit) 
1. Task 1 (extract and print feature descriptors for given image ID) 
2. Task 2 (extract and stores feature descriptors for all images in given folder) 
3. Task 3 (pre-requisite: Task 2; given an image ID- finds 'k' most similar images) 
9. Quit
Option? 2
TASK 2:
Enter the dataset folder path: /home/varun/Desktop/MWDB/Project/input
Output saved in file - 
 /home/varun/Desktop/MWDB/Project/output/cm_folder_09152019_194937.csv
Output for directory /home/varun/Desktop/MWDB/Project/input - STORED

```

For Task 3(choose option 3):
**[NOTE: For Task 3, Task 2 is a pre-requisite]**

```sh
Enter the task option to execute(or 9 to quit) 
1. Task 1 (extract and print feature descriptors for given image ID) 
2. Task 2 (extract and stores feature descriptors for all images in given folder) 
3. Task 3 (pre-requisite: Task 2; given an image ID- finds 'k' most similar images) 
9. Quit
Option? 3
TASK 3:
Enter the dataset folder path: /home/varun/Desktop/MWDB/Project/input
Enter the image id: 0008110
Enter value for 'k' most similar images: 3
Feature descriptor already exists for image ID -  0008110
Details of 'k' most similar images - Image ID : Average euclidean distance(similarity measure)
0008111 : 0.793814627689069
0008130 : 3.9226758384124563
0008129 : 4.694454427825945

```
Finally, to QUIT(choose option 9):

```sh
Enter the task option to execute(or 9 to quit) 
1. Task 1 (extract and print feature descriptors for given image ID) 
2. Task 2 (extract and stores feature descriptors for all images in given folder) 
3. Task 3 (pre-requisite: Task 2; given an image ID- finds 'k' most similar images) 
9. Quit
Option? 9
You opted to quit the demo. Exiting.
```


### Todos
 - Use MongoDB to store & retrieve results
 - Test more similarity measure methods




[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>

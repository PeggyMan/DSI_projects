# **Project 2: Ames Housing Data and Kaggle Challenge**

**Table of Content:**

* [Problem Statement](#Problem-Statement)
* [Executive Summary](#Executive-Summary)
  * [Datasets](#Datasets)
  * [Data Dictionary](#Data-Dictionary)



## **Problem Statement**

What are the features affecting the housing sale price? 



## **Executive Summary**

- I will predict the house sale price by using AmesHousing dataset from Ames, Iowa Assessor’s Office .

  This data set contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010.

  I have identify the correlations or underlying patterns amongst the features in the dataset and the sale price by cleaning data, visualising the statistics number, like the mean, minimum and maximum of the sale price, by using different types of charts.

  Then I evaluate the features by using 3 regression models: `LinearRegression`, `LassoCV` and `RidgeCV`

  I have some useful observations. First of all, quality ratings are have high positive impact then the condition ratings. For example the overall quality has higher corelation than overall condition.

  Secondly, I expected that the lasso model will select a handful of significant features, however, the lasso model flitered half of the features. I belived the performance will be improved by adjusting the alpha value. Thirdly, the predictors of sale price makes sense. The higher correlated predictors are overall quality and the area of the house.



### Datasets

We will use the following two provided datasets for this project:

- [Train.csv](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)
- [Test.csv](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)

This data set contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010.



### Data Dictionary

|     Column      |  Type  | Description                                                  |
| :-------------: | :----: | :----------------------------------------------------------- |
|       id        |  int   | **ID**                                                       |
|       pid       |  int   | **Property ID Number**                                       |
|   ms_subclass   | object | **The building class** <br> 20 : 1-STORY 1946 & NEWER ALL STYLES <br>30 : 1-STORY 1945 & OLDER<br>40 : 1-STORY W/FINISHED ATTIC ALL AGES<br>45 : 1-1/2 STORY - UNFINISHED ALL AGES<br>50 : 1-1/2 STORY FINISHED ALL AGES<br>60 : 2-STORY 1946 & NEWER<br>70 : 2-STORY 1945 & OLDER<br>75 : 2-1/2 STORY ALL AGES<br>80 : SPLIT OR MULTI-LEVEL<br>85 : SPLIT FOYER<br>90 : DUPLEX - ALL STYLES AND AGES<br>120 : 1-STORY PUD (Planned Unit Development) - 1946 & NEWER<br>150 : 1-1/2 STORY PUD - ALL AGES<br>160 : 2-STORY PUD - 1946 & NEWER<br>180 : PUD - MULTILEVEL - INCL SPLIT LEV/FOYER<br>190 : 2 FAMILY CONVERSION - ALL STYLES AND AGES |
|    ms_zoning    | object | **Identifies the general zoning classification of the sale.**<br>A : Agriculture<br>C : Commercial<br>FV : Floating Village Residential<br>I : Industrial<br>RH : Residential High Density<br>RL : Residential Low Density<br>RP : Residential Low Density Park<br>RM : Residential Medium Density |
|  lot_frontage   | float  | **Linear feet of street connected to property**              |
|    lot_area     |  int   | **Lot size in square feet**                                  |
|     street      | object | **Type of road access to property**<br>Grvl : Gravel<br>Pave : Paved |
|      alley      | object | **Type of alley access to property**<br>Grvl : Gravel<br>Pave : Paved<br>NA : No alley access |
|    lot_shape    | object | **LotShape: General shape of property**<br>Reg : Regular<br>IR1 : Slightly irregular<br>IR2 : Moderately Irregular<br>IR3 : Irregular |
|  land_contour   | object | **LandContour: Flatness of the property**<br>Lvl : Near Flat/Level<br>Bnk : Banked - Quick and significant rise from street grade to building<br>HLS : Hillside - Significant slope from side to side<br>Low Depression |
|    utilities    | object | **Type of utilities available**<br>AllPub : All public Utilities (E,G,W,& S)<br>NoSewr : Electricity, Gas, and Water (Septic Tank)<br>NoSeWa : Electricity and Gas Only<br>ELO : Electricity only |
|   lot_config    | object | **Lot configuration**<br>Inside : Inside lot<br>Corner : Corner lot<br>CulDSac : Cul-de-sac<br>FR2 : Frontage on 2 sides of property<br>FR3 : Frontage on 3 sides of property |
|   land_slope    |  int   | **Slope of property**<br>Gtl : Gentle slope<br>Mod : Moderate Slope<br>Sev : Severe Slope |
|  neighborhood   | object | **Physical locations within Ames city limits**<br>Blmngtn : Bloomington Heights<br>Blueste : Bluestem<br>BrDale : Briardale<br>BrkSide : Brookside<br>ClearCr : Clear Creek<br>CollgCr : College Creek<br>Crawfor : Crawford<br>Edwards : Edwards<br>Gilbert : Gilbert<br>IDOTRR : Iowa DOT and Rail Road<br>Meadow : Meadow Village<br>Mitchel : Mitchell<br>Names : North Ames<br>NoRidge : Northridge<br>NPkVill : Northpark Villa<br>NridgHt : Northridge Heights<br>NWAmes : Northwest Ames<br>OldTown : Old Town<br>SWISU : South & West of Iowa State University<br>Sawyer : Sawyer<br>SawyerW : Sawyer West<br>Somerst : Somerset<br>StoneBr : Stone Brook<br>Timber : Timberland<br>Veenker : Veenker |
|   condition_1   | object | **Proximity to main road or railroad**<br>Artery : Adjacent to arterial street<br>Feedr : Adjacent to feeder street<br>Norm : Normal<br>RRNn : Within 200' of North-South Railroad<br>RRAn : Adjacent to North-South Railroad<br>PosN : Near positive off-site feature--park, greenbelt, etc.<br>PosA : Adjacent to postive off-site feature<br>RRNe : Within 200' of East-West Railroad<br>RRAe : Adjacent to East-West Railroad |
|   condition_2   | object | **Proximity to main road or railroad (if a second is present)**<br>Artery : Adjacent to arterial street<br>Feedr : Adjacent to feeder street<br>Norm : Normal<br>RRNn : Within 200' of North-South Railroad<br>RRAn : Adjacent to North-South Railroad<br>PosN : Near positive off-site feature--park, greenbelt, etc.<br>PosA : Adjacent to postive off-site feature<br>RRNe : Within 200' of East-West Railroad<br>RRAe : Adjacent to East-West Railroad |
|    bldg_type    | object | **Type of dwelling**<br>1Fam : Single-family Detached<br>2FmCon : Two-family Conversion; originally built as one-family dwelling<br>Duplx : Duplex<br>TwnhsE : Townhouse End Unit<br>TwnhsI : Townhouse Inside Unit |
|   house_style   | object | **Style of dwelling**<br>1Story : One story<br>1.5Fin : One and one-half story: 2nd level finished<br>1.5Unf : One and one-half story: 2nd level unfinished<br>2Story : Two story<br>2.5Fin : Two and one-half story: 2nd level finished<br>2.5Unf : Two and one-half story: 2nd level unfinished<br>SFoyer : Split Foyer<br>SLvl : Split Level |
|  overall_qual   |  int   | **Overall material and finish quality**<br>10 : Very Excellent<br>9 : Excellent<br>8 : Very Good<br>7 : Good<br>6 : Above Average<br>5 : Average<br>4 : Below Average<br>3 : Fair<br>2 : Poor<br>1 : Very Poor |
|  overall_cond   |  int   | **Overall condition rating**<br>10 : Very Excellent<br>9 : Excellent<br>8 : Very Good<br>7 : Good<br>6 : Above Average<br>5 : Average<br>4 : Below Average<br>3 : Fair<br>2 : Poor<br>1 : Very Poor |
|   year_built    |  int   | **Original construction date**                               |
| year_remod/add  |  int   | **Remodel date (same as construction date if no remodeling or additions)** |
|   roof_style    | object | **Type of roof**<br>Flat : Flat<br>Gable : Gable<br>Gambrel : Gabrel (Barn)<br>Hip : Hip<br>Mansard : Mansard<br>Shed : Shed |
|    roof_matl    | object | **Roof material**<br>ClyTile : Clay or Tile<br>CompShg : Standard (Composite) Shingle<br>Membran : Membrane<br>Metal : Metal<br>Roll : Roll<br>Tar&Grv : Gravel & Tar<br>WdShake : Wood Shakes<br>WdShngl : Wood Shingles |
|  exterior_1st   | object | **Exterior covering on house**<br>AsbShng : Asbestos Shingles<br>AsphShn : Asphalt Shingles<br>BrkComm : Brick Common<br>BrkFace : Brick Face<br>CBlock : Cinder Block<br>CemntBd : Cement Board<br>HdBoard : Hard Board<br>ImStucc : Imitation Stucco<br>MetalSd : Metal Siding<br>Other : Other<br>Plywood : Plywood<br>PreCast : PreCast<br>Stone : Stone<br>Stucco : Stucco<br>VinylSd : Vinyl Siding<br>Wd Sdng : Wood Siding<br>WdShing : Wood Shingles |
|  exterior_2nd   | object | **Exterior covering on house (if more than one material)**<br>AsbShng : Asbestos Shingles<br>AsphShn : Asphalt Shingles<br>BrkComm : Brick Common<br>BrkFace : Brick Face<br>CBlock : Cinder Block<br>CemntBd : Cement Board<br>HdBoard : Hard Board<br>ImStucc : Imitation Stucco<br>MetalSd : Metal Siding<br>Other : Other<br>Plywood : Plywood<br>PreCast : PreCast<br>Stone : Stone<br>Stucco : Stucco<br>VinylSd : Vinyl Siding<br>Wd Sdng : Wood Siding<br>WdShing : Wood Shingles |
|  mas_vnr_type   | object | **Masonry veneer type**<br>BrkCmn : Brick Common<br>BrkFace : Brick Face<br>Block : Cinder Block<br>None : None<br>Stone : Stone |
|  mas_vnr_area   | float  | **Masonry veneer area in square feet**                       |
|   exter_qual    |  int   | **Exterior material quality**<br>Ex : Excellent<br>Gd : Good<br>TA : Average/Typical<br>Fa : Fair<br>Po : Poor |
|   exter_cond    |  int   | **Present condition of the material on the exterior**<br>Ex : Excellent<br>Gd : Good<br>TA : Average/Typical<br>Fa : Fair<br>Po : Poor |
|   foundation    | object | **Type of foundation**<br>BrkTil : Brick & Tile<br>CBlock : Cinder Block<br>PConc : Poured Contrete<br>Slab : Slab<br>Stone : Stone<br>Wood : Wood |
|    bsmt_qual    |  int   | **Height of the basement**<br>Ex : Excellent (100+ inches)<br>Gd : Good (90-99 inches)<br>TA : Typical (80-89 inches)<br>Fa : Fair (70-79 inches)<br>Po : Poor (<70 inches)<br>NA : No Basement |
|    bsmt_cond    |  int   | General condition of the basement<br>Ex : Excellent<br>Gd : Good<br>TA : Typical - slight dampness allowed<br>Fa : Fair - dampness or some cracking or settling<br>Po : Poor - Severe cracking, settling, or wetness<br>NA : No Basement |
|  bsmt_exposure  |  int   | **Walkout or garden level basement walls**<br>Gd : Good Exposure<br>Av : Average Exposure (split levels or foyers typically score average or above)<br>Mn : Mimimum Exposure<br>No : No Exposure<br>NA : No Basement |
| bsmtfin_type_1  | object | **Quality of basement finished area**<br>GLQ : Good Living Quarters<br>ALQ : Average Living Quarters<br>BLQ : Below Average Living Quarters<br>Rec : Average Rec Room<br>LwQ : Low Quality<br>Unf : Unfinshed<br>NA : No Basement |
|  bsmtfin_sf_1   | float  | **Type 1 finished square feet**                              |
| bsmtfin_type_2  | object | **Quality of second finished area (if present)**<br>GLQ : Good Living Quarters<br>ALQ : Average Living Quarters<br>BLQ : Below Average Living Quarters<br>Rec : Average Rec Room<br>LwQ : Low Quality<br>Unf : Unfinshed<br>NA : No Basement |
|  bsmtfin_sf_2   | float  | **Type 2 finished square feet**                              |
|   bsmt_unf_sf   | float  | **Unfinished square feet of basement area**                  |
|  total_bsmt_sf  | float  | **Total square feet of basement area**                       |
|     heating     | object | **Type of heating**<br>Floor : Floor Furnace<br>GasA : Gas forced warm air furnace<br>GasW : Gas hot water or steam heat<br>Grav : Gravity furnace<br>OthW : Hot water or steam heat other than gas<br>Wall : Wall furnace |
|   heating_qc    |  int   | **Heating quality and condition**<br>Ex : Excellent<br>Gd : Good<br>TA : Average/Typical<br>Fa : Fair<br>Po : Poor |
|   central_air   |  int   | **Central air conditioning**<br>N : No<br>Y : Yes            |
|   electrical    | object | **Electrical system**<br>SBrkr : Standard Circuit Breakers & Romex<br>FuseA : Fuse Box over 60 AMP and all Romex wiring (Average)<br>FuseF : 60 AMP Fuse Box and mostly Romex wiring (Fair)<br>FuseP : 60 AMP Fuse Box and mostly knob & tube wiring (poor)<br>Mix : Mixed |
|   1st_flr_sf    | float  | **First Floor square feet**                                  |
|   2nd_flr_sf    | float  | **Second floor square feet**                                 |
| low_qual_fin_sf | float  | **Low quality finished square feet (all floors)**            |
|   gr_liv_area   | float  | **Above grade (ground) living area square feet**             |
| bsmt_full_bath  |  int   | **Basement full bathrooms**                                  |
| bsmt_half_bath  |  int   | **Basement half bathrooms**                                  |
|    full_bath    |  int   | **Full bathrooms above grade**                               |
|    half_bath    |  int   | **Half baths above grade**                                   |
|  bedroom_abvgr  |  int   | **Number of bedrooms above basement level**                  |
|  kitchen_abvgr  |  int   | **Number of kitchens**                                       |
|  kitchen_qual   |  int   | **Kitchen quality**<br>Ex : Excellent<br>Gd : Good<br>TA : Typical/Average<br>Fa : Fair<br>Po : Poor |
|  totrms_abvgrd  |  int   | **Total rooms above grade (does not include bathrooms)**     |
|   functional    | object | **Home functionality rating**<br>Typ : Typical Functionality<br>Min1 : Minor Deductions 1<br>Min2 : Minor Deductions 2<br>Mod : Moderate Deductions<br>Maj1 : Major Deductions 1<br>Maj2 : Major Deductions 2<br>Sev : Severely Damaged<br>Sal : Salvage only |
|   fireplaces    |  int   | **Number of fireplaces**                                     |
|  fireplace_qu   | object | **Fireplace quality**<br>Ex : Excellent - Exceptional Masonry Fireplace<br>Gd : Good - Masonry Fireplace in main level<br>TA : Average - Prefabricated Fireplace in main living area or Masonry Fireplace in basement<br>Fa : Fair - Prefabricated Fireplace in basement<br>Po : Poor - Ben Franklin Stove<br>NA : No Fireplace |
|   garage_type   | object | **Garage location**<br>2Types : More than one type of garage<br>Attchd : Attached to home<br>Basment : Basement Garage<br>BuiltIn : Built-In (Garage part of house - typically has room above garage)<br>CarPort : Car Port<br>Detchd : Detached from home<br>NA : No Garage |
|  garage_yr_blt  |  int   | **Year garage was built**                                    |
|  garage_finish  |  int   | **Interior finish of the garage**<br>Fin : Finished<br>RFn : Rough Finished<br>Unf : Unfinished<br>NA : No Garage |
|   garage_cars   |  int   | **Size of garage in car capacity**                           |
|   garage_area   | float  | **Size of garage in square feet**                            |
|   garage_qual   |  int   | **Garage quality**<br>Ex : Excellent<br>Gd : Good<br>TA : Typical/Average<br>Fa : Fair<br>Po : Poor<br>NA : No Garage |
|   garage_cond   |  int   | **Garage condition**<br>Ex : Excellent<br>Gd : Good<br>TA : Typical/Average<br>Fa : Fair<br>Po : Poor<br>NA : No Garage |
|   paved_drive   | object | **Paved driveway**<br>Y : Paved<br>P : Partial Pavement<br>N : Dirt/Gravel |
|  wood_deck_sf   | float  | **Wood deck area in square feet**                            |
|  open_porch_sf  | float  | **Open porch area in square feet**                           |
| enclosed_porch  | float  | **Enclosed porch area in square feet**                       |
|   3ssn_porch    | float  | **Three season porch area in square feet**                   |
|  screen_porch   | float  | **Screen porch area in square feet**                         |
|    pool_area    |  int   | **Pool area in square feet**                                 |
|     pool_qc     | object | **Pool quality**<br>Ex : Excellent<br>Gd : Good<br>TA : Average/Typical<br>Fa : Fair<br>NA : No Pool |
|      fence      | object | **Fence quality**<br>GdPrv : Good Privacy<br>MnPrv : Minimum Privacy<br>GdWo : Good Wood<br>MnWw : Minimum Wood/Wire<br>NA : No Fence |
|  misc_feature   | object | **Miscellaneous feature not covered in other categories**<br>Elev : Elevator<br>Gar2 : 2nd Garage (if not described in garage section)<br>Othr : Other<br>Shed : Shed (over 100 SF)<br>TenC : Tennis Court<br>NA : None |
|    misc_val     |  int   | **$Value of miscellaneous feature**                          |
|     mo_sold     |  int   | **Month Sold**                                               |
|     yr_sold     |  int   | **Year Sold**                                                |
|    sale_type    | object | **Type of sale**<br>WD : Warranty Deed - Conventional<br>CWD : Warranty Deed - Cash<br>VWD : Warranty Deed - VA Loan<br>New : Home just constructed and sold<br>COD : Court Officer Deed/Estate<br>Con : Contract 15\% Down payment regular terms<br>ConLw : Contract Low Down payment and low interest<br>ConLI : Contract Low Interest<br>ConLD : Contract Low Down<br>Oth : Other |
|    saleprice    |  int   | **Property's sale price in dollars**                         |
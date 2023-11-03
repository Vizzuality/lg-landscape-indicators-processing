# Land, carbon and biodiversity data for supply chain impact calculation

This repository contains global gridded data for estimating supply chain impacts relating to deforestation, related greenhouse gas emissions, conversion of natural ecosystems, and loss of intact or high integrity ecosystems. These data were originally prepared for the LandGriffon service (https://landgriffon.com) following international standards and guidelines for reporting and target setting in the agriculture, forestry, and land use sector. In particular, they employ a spatial adaptation of the Statistical Land Use Change (sLUC) by land occupation accounting method in which responsibility for impacts are allocated across a 50km radius instead of across a jurisdiction.

Methodology and usage notes: https://www.biorxiv.org/content/10.1101/2023.11.01.565036v1

Code: https://github.com/Vizzuality/lg-landscape-indicators-processing

Five indicators are included, with two layers per indicator: the impact, and annualized impact per hectare of human land use.

**Impact layers (100m)**

| file | indicator | units |
| --- | --- | --- |
| deforest_100m_cog.tif | Deforestation (2002-2022) | portion of cell |
| deforest_carbon_100m_cog.tif | Deforestation carbon (2002-2022) | tC/ha |
| natcrop_expansion_100m_cog.tif | Cropland expansion in natural ecosystems (2020-2022) | portion of cell |
| natcrop_reduction_100m_cog.tif | Cropland reduction in natural ecosystems (2020-2022) | portion of cell |
| natcrop_bii_100m_cog.tif | Biodiversity Intactness score of converted areas | score |
| natcrop_fii_100m_cog.tif | Forest Landscape Integrity Index of converted areas | score |

**Annualized impact per hectare of human land use (1000m)**

| file | indicator | units |
| --- | --- | --- |
| deforest_by_human_lu_50km_1000m_cog.tif | Deforestation | ha/yr / haLU |
| deforest_carbon_by_human_lu_50km_1000m_cog.tif | Deforestation carbon emissions | tCO2/yr / haLU |
| natural_crop_net_conversion_by_human_lu_50km_1000m_cog.tif | Net cropland expansion in natural lands | ha/yr / haLU |
| natural_crop_bii_loss_by_human_lu_50km_1000m_cog.tif | Loss of forest integrity to cropland expansion | score / haLU |
| natural_crop_flii_loss_by_human_lu_50km_1000m_cog.tif | Loss of biodiversity intactness to cropland expansion | score / haLU |

Of note, these datasets are not constrained to areas of current human land use, e.g. such that land use in remote wilderness may be assigned a maximum impact score.

See https://landgriffon.com/methodology for techniques for combining these results with land footprint data and production data to calculate the impacts of raw materials sourced from for local, regional, or national supply-sheds. For example, to calculate the deforestation footprint of sourcing 100 tons of soy from Argentina, a user could first calculate the average hectares of deforestation per hectare of land use for all soy producing areas in Argentina, and then multiply that value by the land footprint of 100 tons of soy production.

### License

(c) Vizzuality 2023 CC-BY. This data is made available under a Creative Commons Attribution 4.0 International [license](https://creativecommons.org/licenses/by/4.0/).

### Suggested citation

Francis Gassert, Biel Stela, Elena Palao Martinez, and Michael Harfoot. 2023. “Land, Carbon and Biodiversity Data for Supply Chain Impact Calculations.” Preprint. BioRxiv, 2023.11.01.565036. https://doi.org/10.1101/2023.11.01.565036.

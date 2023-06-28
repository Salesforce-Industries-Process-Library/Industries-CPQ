# Industries-CPQ

## Attribute Based Pricing

The `AttributeBasedPricing.zip` contains the following Apex Classes:
- PricingPlanHelper
- CustomPricingPlanStempImpl
- CustomPricingPlanStempImplTest
- AttributeMatrixInfoCacheBatch
- CpqNextPricingPlanHelper
- CpqNextPricingPlanHelperTest

Follow the below steps to deploy the `AttributeBasedPricing.zip` in an Org:

1. Go to Workbench -> migration -> Deploy
2. Choose the AttributeBasedPricing.zip file.
3. Check the Single Package checkbox.
4. Click Next -> Deploy
5. In the Results section, verify -> success: <span style="color: green;">true</span>

The `AttributeBasedPricing_MultiPack.json` contains the following sample Calculation Procedures and Calculation Matrices:
- Calculation Procedures:
    1. AttributePricingProcedure 
        - CalculationProcedureVersion: AttributePricingProcedure v1 
        - CalculationProcedureVariable:
            - REC_MNTH_STD_PRC
            - OT_STD_PRC 
            - Source Product Name 
            - Source Product Code 
            - Characteristic Name 
            - Characteristic Value 
            - NRC 
            - MRC
    2. RangeAttributePricingProcedure 
        - CalculationProcedureVersion: RangeAttributePricingProcedure V1 
        - CalculationProcedureVariable:
            - NRC 
            - MRC 
            - Characteristic Code 
            - REC_MNTH_STD_PRC 
            - OT_STD_PRC 
            - Source Product Name 
            - Source Product Code 
            - Characteristic Name 
            - Characteristic Value 
            - Quantity 
            - MRC 
            - NRC 
    3. SourceTargetAttributePricingProcedure 
        - CalculationProcedureVersion: SourceTargetAttributePricingProcedure v1 
        - CalculationProcedureVariable:
            - REC_MNTH_STD_PRC 
            - OT_STD_PRC 
            - Source Product Name 
            - Source Product Code 
            - Characteristic Name 
            - Characteristic Value 
            - Target Product Name 
            - MRC
            - NRC 
            - NRC
            - Target Product Name 
            - MRC
    4. VolumeRangeAttributePricingProcedure
        - CalculationProcedureVersion: VolumeRangeAttributePricingProcedure V1 
        - CalculationProcedureVariable:
            - NRC
            - MRC 
            - Quantity 
            - Source Product Name 
            - Source Product Code 
            - REC_MNTH_STD_PRC 
            - OT_STD_PRC 
            - MRC 
            - NRC
- Calculation Matrices:
    1. AttributePricingMatrix
        - CalculationMatrixVersion: AttributePricingMatrix v2 
    2. RangeAttributePricingMatrix
        - CalculationMatrixVersion: RangeAttributePricingMatrix v1
    3. SourceTargetAttributePricingMatrix
        - CalculationMatrixVersion: SourceTargetAttributePricingMatrix v2 
    4. VolumeRangeAttributePricingMatrix
        - CalculationMatrixVersion: VolumeRangeAttributePricingMatrix v4

Follow the below steps to deploy the `AttributeBasedPricing_MultiPack.json` in an Org:

1. Go to Vlocity Cards.
2. Click on the Import button.
3. Upload the `AttributeBasedPricing_MultiPack.json` file.
4. Import and activate the datapack.
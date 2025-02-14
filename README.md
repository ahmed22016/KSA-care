# KSA-care
#Beneficiaries of care services for children with disabilities
#DATASET ACTIVATE DataSet1.
#LOGISTIC REGRESSION VARIABLES servic
  /METHOD=ENTER sex العمر edu_2cat dis_type region 
  /CONTRAST (sex)=Indicator(1)
  /CONTRAST (region)=Indicator
  /CONTRAST (dis_type)=Indicator
  /CONTRAST (edu_2cat)=Indicator(1)
  /PRINT=GOODFIT
  /CRITERIA=PIN(0.05) POUT(0.10) ITERATE(20) CUT(0.5).

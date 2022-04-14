3D-HST data consists of 4 parts: SCI_image, PSF_image, ACS_exp_map, 3D-HST_cat.fits
SCI_image: contains the drizzled and aligned multi-band science image of the entire survey field, which can be separated into 3 different field, COSMOS, GOODS-s and UDS;
PSF_image: containts the standard stacked point-spread-function of different band in different field
ACS_exp_map: lenstronomy requires background noise distribution to do weighting during fitting, exposure time is vital for lenstronomy to estimate background noise level;
	all of the SCI_image contains exposure time in its header except F606W and F814W in COSMOS field; the exposure time of these two band is in the fits file of exposure map in ACS_exp_map directory;

3D-HST_cat.fits: this is the catalogue of the 17 sources in 3D-HST survey;
meaning of each row:
	ID: source id in the original catalogue, not very important
	Field: field of the source
	RAdeg: J2000 right ascension in degree
	DEdeg: J2000 declination in degree
	x: x axis pixel number in SCI_image
	y: yaxis pixel number in SCI_image
	zpk: redshift
	F125W ~ F850LP: target flux in different band, the target has a solid detection as long as the value is not -99, specific number is not important;
	Mbh: log(bh_mass/sun_mass)
	Mbh_err: measurement error
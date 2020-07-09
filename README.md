# Analysis of High Energy Theory postdoc applicants
Latest interactive visualizations can be found [here](http://wwwhome.lorentz.leidenuniv.nl/~garnier/).

This project presents relevant statistics concerning successful applicants for high-energy theory postdoc positions. Identity of successful applicants was obtained from the [HEP-TH rumor mill](https://sites.google.com/site/postdocrumor/) and analyzed for application years 2017-2020. This data is self-reported which introduces some bias. And of course, no data is available about unsucessful applicants.

Using the identity of each applicant, publication details were obtained using the [old InspireHEP](http://old.inspirehep.net) [API](http://old.inspirehep.net/info/hep/api). For years earlier than 2020, statistics were modified to reflect the situation at the time of application. This was done by bulk-downooading Inspire records and building a SQL database on AWS to avoid making numerous (slow) API calls. 

The applicant's position at the time of application (PhD student or Postdoc) could not be easily obtained by API calls. Therefore, applicants for 2020 were hand-labelled and a model was built to label applicants of previous years based on time since publication of first and second paper, number of listed affiliations and whether the applicant was part of a large collaboration. This model achieved 90% accuracy on a test set. This introduces an inherent uncertainty in the split between PhD and Postdoc applicants compared to the combined numbers. 

Code for downloading data and processing it, as well as for training the PhD/Postdoc classifier, can be found in the '**rumors**' notebook. Some static visualizations as well as code for creating dynamic plotly visualizations is in the '**rumor_visualizations**' notebook. 

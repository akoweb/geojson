# geojson
province of iran - json data for leafletjs and openstreetmap


sample


after import https://leafletjs.com/ lib

		
$.getJSON('db/iran-province.json', function (allprovince) {
	
	 

				for (var i in allprovince ) {
 
											
					 var latlng = L.latLng({
					 lat: allprovince[i].latitude,
					 lng: allprovince[i].longitude
					 });
					 
					
					var final_icons =L.icon({ iconUrl: 'images/province.png', iconSize: [52,52]});
 
			 L.marker(latlng, {title:allprovince[i].slug, icon:final_icons}).bindPopup( allprovince[i].slug+'<br/>'+allprovince[i].title ).addTo(lay_provinces);
	 
 
										
												
												
				}
				
				 
				  
				 
				
 


});				
				

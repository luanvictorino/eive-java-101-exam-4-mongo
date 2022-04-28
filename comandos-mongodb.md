* Importar banco:
 	```
 	mongoimport listingsAndReviews.json
 	```

* Acessar o mongoDb:
 	```
 	mongo
 	```

* Acessar o banco:
 	```
 	use airbnbdb
 	```

* Criar uma collection:
 	```
 	db.createCollection('airbnb')
	```

* Incluir um novo registro:
 	```
	 db.airbnb.insertOne({
	    _id: '9999990',
	    listing_url: 'https://www.airbnb.com/rooms/9999990',
	    name: 'Apartamento de luxo em Copacabana - 4 quartos',
	    summary: 'Meu espaço é bom para casais, viajantes de negócios e famílias (com crianças).',
	    space: '',
	    description: 'Meu espaço é bom para casais, viajantes de negócios e famílias (com crianças).',
	    neighborhood_overview: '',
	    notes: '',
	    transit: '',
	    access: '',
	    interaction: '',
	    house_rules: '',
	    property_type: 'Apartment',
	    room_type: 'Entire home/apt',
	    bed_type: 'Real Bed',
	    minimum_nights: '1',
	    maximum_nights: '1125',
	    cancellation_policy: 'flexible',
	    last_scraped: ISODate('2019-02-11T05:00:00Z'),
	    calendar_last_scraped: ISODate('2019-02-11T05:00:00Z'),
	    accommodates: 8,
	    bedrooms: 4,
	    beds: 4,
	    number_of_reviews: 0,
	    bathrooms: NumberDecimal('4.5'),
	    amenities: [
	        'TV',
	        'Wifi',
	        'Air conditioning',
	        'Kitchen',
	        'Free parking on premises',
	        'Gym',
	        'Breakfast',
	        'Elevator',
	        'Washer',
	        'Dryer',
	        'Fire extinguisher',
	        'Essentials',
	        'Shampoo',
	        'Lock on bedroom door',
	        'Hair dryer',
	        'Iron'
	    ],
	    price: NumberDecimal('11190.00'),
	    extra_people: NumberDecimal('0.00'),
	    guests_included: NumberDecimal('1'),
	    images: {
	        thumbnail_url: '',
	        medium_url: '',
	        picture_url: 'https://a0.muscache.com/im/pictures/56d27407-f610-48f8-9adf-3387adc1d286.jpg?aki_policy=large',
	        xl_picture_url: ''
	    },
	    host: {
	        host_id: '26227035',
	        host_url: 'https://www.airbnb.com/users/show/26227035',
	        host_name: 'Giovana',
	        host_location: 'Barra da Tijuca, State of Rio de Janeiro, Brazil',
	        host_about: '',
	        host_thumbnail_url: 'https://a0.muscache.com/im/pictures/8a811dfe-ba5c-4168-a781-934ab0261c32.jpg?aki_policy=profile_small',
	        host_picture_url: 'https://a0.muscache.com/im/pictures/8a811dfe-ba5c-4168-a781-934ab0261c32.jpg?aki_policy=profile_x_medium',
	        host_neighbourhood: 'Copacabana',
	        host_is_superhost: false,
	        host_has_profile_pic: true,
	        host_identity_verified: false,
	        host_listings_count: 1,
	        host_total_listings_count: 1,
	        host_verifications: [
	            'email',
	            'phone',
	            'jumio',
	            'government_id'
	        ]
	    },
	    address: {
	        street: 'Rio de Janeiro, Rio de Janeiro, Brazil',
	        suburb: 'Copacabana',
	        government_area: 'Copacabana',
	        market: 'Rio De Janeiro',
	        country: 'Brazil',
	        country_code: 'BR',
	        location: {
	            type: 'Point',
	            coordinates: [-43.19373213382171, -22.97691478494771],
	            is_location_exact: true
	        }
	    },
	    availability: {
	        availability_30: 29,
	        availability_60: 59,
	        availability_90: 89,
	        availability_365: 364
	    },
	    review_scores: {},
	    reviews: []
	})
 	```

* Alterar o registro incluído:
 	```
 	db.airbnb.updateOne({_id:"9999990"},{$set:{price:NumberDecimal("500.00")}})
 	```

* Consultar um registro:
	```
	db.airbnb.find({"address.country_code":"BR"},{_id:0}).sort({price:-1}).limit(1)
	```
The problem
India throws away crores of rupees of recyclable scrap every month. Selling raddi still means waiting for a kabadiwala who may never come. The seller can't check his scale, doesn't know what a fair rate is, and old gadgets get paid for by weight even when they still work. Kabadiwalas, for their part, lose hours roaming lanes looking for work.

Apna Scrap turns this into an Uber-style marketplace:

Sellers photograph their scrap. AI names every item, estimates its weight and prices it at their town's rate.
Partners (kabadiwalas, recyclers, EV-scooty and e-rickshaw owners) get nearby jobs with the seller's own photo.
The platform picks the right vehicle, dispatches the best free partner, tracks the pickup live, bills from a digital scale, and takes a small commission.
Screenshots
Home	Scrap Lens	Live tracking	Sign in
Website: home	Website: sell with a photo
Features
📷 Scrap Lens: AI that reads your photo
The scanner works like a visual search app. It goes through four steps, and you watch each one happen:

On device: TF.js COCO-SSD draws boxes around everyday objects in under a second.
Vision model: Claude looks at the whole photo, using those boxes as hints. For every item it returns the name, material, count, size in cm, condition, its own weight guess and a bounding box. It also lists anything that's banned. Item names stream in as they're written.
Physics check: every weight is compared with what that many pieces, or that volume of the material, normally weighs. If the AI is more than 2× off, the weight is pulled back and the line is marked Checked (so "3 phones = 9 kg" becomes about 1 kg).
Local rate: the checked weight is priced at the seller's hub rate.
You can fix any count and the line is checked and priced again. The server re-validates every reading a browser sends, so a forged reading can't set its own price.

Pricing for every town in India
36 states and UTs and 4,373 towns, all offline.
Rate = national base × state × city × hub distance, shown line by line. The seller can ask ±15%.
Location can be found by GPS automatically when the app opens, by searching a town or pincode, by tapping the India map, or by pasting from Google Maps.

AI dispatch with the right vehicle
One tap picks the vehicle for the load and the best free partner (ETA, rating, vehicle fit, wallet), and shows the reasons and which partners it skipped.
Two-wheelers and EV scooties take e-waste only, up to 30 kg. Paper, plastic, metal and bigger loads go to an e-rickshaw or larger.

Track it like a ride
Live map (Leaflet + OpenStreetMap + OSRM road routes), with "arrives around 4:42 pm" ETA alerts.
A ride-app style arrival call through a masked number.
An OTP at the door, then the digital scale and the bill.

Paid your way
UPI (ID validated, with a UPI QR on the partner side), debit card (Luhn check, network, expiry; only the last four digits are kept) or cash at pickup.
The bill always uses the scale reading, never the AI guess.

Safe by design
E-waste is graded A to D (working, repairable, parts, recycle) and priced by grade, so a working phone is paid as a phone.
Medical, hazardous and illegal items are blocked at the scan step, with safe-disposal advice. Swollen batteries, CRTs and CFLs are refused.

Sign in like other apps
The home page opens first. Sellers can browse and price without an account, and sign in when they book.
Sign-in is by mobile + 6-digit OTP or Continue with Google (then a verified mobile), followed by a "Turn on your location" screen.
The partner app needs an account.


One codebase, two experiences
A phone app (seller app and partner app) and a separate desktop website that works like a shopping site, with a search header, rate results, checkout-style selling and sign-in at checkout.
Both are built from the same core and components.

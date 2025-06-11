# PinPoint: Stay Alert, Stay Safe
PinPoint is currently in a closed beta state, currently registration is exlusively available to students of the University of California, Santa Cruz (UCSC). If you are a UCSC student, please feel free to reach out for access to the beta build. You can still access the application and server by hosting a local development deployment of the app on your machine, provided you have a mobile device to connect to.

You can view a video demo here: https://www.youtube.com/watch?v=mv7kUvMTjF0

### Installation Guide | Locally Hosted Instance
If you wish to host a local instance of PinPoint, follow the instructions below.

Before you begin, you will need NodeJS and Node Package Manager (npm) installed on your machine. You will also need the Expo Go app installed on your mobile device.

Clone the repository.
```
git clone https://github.com/adamnmartinez/pinpointapp.git
```

Go into the "frontend" directory and install the required packages.
```
cd frontend
npm install
```

Run `npx expo start` to start the mobile deployment. 
- Try `npx expo start --tunnel` if the standard connection fails to connect.

Scan the QR code generated in your console with your mobile device to connect to the development build. 

#### Additonal Instructions - Backend Deployment
If you wish to host your own server with the app, perform the following additonal instructions. You will need a PostgreSQL instance to connect to.

Go into the "backend" directory and install the required packages.
```
cd backend
npm install
```

You'll need to create an environment file named `.env` and place it within the "backend" folder. The file should look like this:
```
PG_HOST=<YOUR DATABASE HOST URL>
PG_PORT=<YOUR DATABASE HOST PORT>
PG_USER=<YOUR DATABASE USERNAME>
PG_PASSWORD=<YOUR DATABASE PASSWORD>
PG_DATABASE=<YOUR DATABASE NAME>

MAIL_HOST = smtp.gmail.com (FOR GMAIL)
MAIL_USER = <YOUR E-MAIL ADDRESS>
MAIL_PASS = <YOUR E-MAIL PASSWORD>
MAIL_PORT = 587 (FOR GMAIL)

HOSTNAME = <YOUR HOST URL>
SECRET_KEY = <YOUR ENCRYPTION KEY>
```

In the "frontend" directory within the `server.tsx` file, you must change the HOST variable to the address of your server.

To start the backend server, run `npm start` in the backend directory.




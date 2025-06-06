# PinPoint: Stay Alert, Stay Safe

### Installation Guide
Before you begin, you will need NodeJS and Node Package Manager (npm) installed on your machine. You will also need the Expo Go app installed on your mobile device.

Clone the repository.
```
git clone https://github.com/adamnmartinez/cse115a.git
```

Go into both directories and install the required packages.
```
cd backend
npm install
...

cd frontend
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

To start the backend server, run `npm start` in the backend directory

In a new tab, move into the `PinPoint` directory within `frontend`. 

In the `server.tsx` file, change the HOST variable to the URL of your backend server. If you are running the frontend deployment on the same machine as the server, you can use `localhost` with the port for your server.

Run `npx expo start` to start the mobile deployment. 
- Try `npx expo start --tunnel` if the standard connection fails to connect.

Scan the QR code generated in your console with your mobile device to connect to the development build. 


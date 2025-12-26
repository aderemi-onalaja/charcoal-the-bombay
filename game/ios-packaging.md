## iOS packaging (Capacitor)

> Planned workflow once the web build is stable.

1. Add Capacitor  
   `npm install @capacitor/core @capacitor/cli`

2. Initialise  
   `npx cap init`

3. Add iOS platform  
   `npm install @capacitor/ios`  
   `npx cap add ios`

4. Build web + sync  
   `npm run build`  
   `npx cap sync ios`

5. Open in Xcode  
   `npx cap open ios`

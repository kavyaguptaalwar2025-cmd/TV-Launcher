# Mera Apple TV style launcher (bina ADB / wireless debugging ke)

## APK kaise banaye (computer par kuch install nahi)
1. github.com par free account banao, is folder ko apni repo mein upload karo (ya "Fork" karo).
2. Repo > Actions > "Build my launcher APK" > Run workflow.
3. 3-5 minute baad run ke andar "tv-launcher-apk" artifact download karo, zip kholo: app-release.apk.

## TV par install (ADB ke bina)
1. APK ko pendrive mein copy karo.
2. TV par Play Store se "Send Files to TV" ya "X-plore" / "File Commander" install karo.
3. Settings > Security > "Unknown sources" us file-manager ke liye ON karo.
4. File manager mein pendrive kholo, APK par OK dabao, Install.
5. Home dabao. Agar chooser aaye to is launcher ko "Always" chuno. Nahi aaye to
   launcher ki Settings mein "Default home" chuno.

Is launcher ke andar: dock ke apps/order badalna (hold OK on tile > Move), App library se apps
add/remove karna. Stock launcher disable karne ke liye ADB chahiye; bina ADB ke woh chalta rehta hai.

## Jo isme NAHI hai (sach)
- Debloat / system apps disable: ADB chahiye. Bina ADB sirf Settings > Apps se khud kar sakte ho.
- Ad blocking: Settings > Network > Private DNS (hostname) `dns.adguard-dns.com` (Android 9+).
  YouTube ads nahi hatenge. Router par Pi-hole/AdGuard ho to router par hi block karo.
- Live TV / Inputs kuch TV par vendor-specific hote hain; model pata chalne par config set hoga.

## Config badalna
launcher/app/src/main/res/values/config.xml: `columns` (dock slots 4-7), `dock_apps` (package names), `dock_glass`.
Badalne ke baad workflow dobara chalao (push par apne aap chalta hai).

## Wapas pehle jaisa
Settings > Apps > is launcher ko Uninstall; Home dobara stock launcher kholega.

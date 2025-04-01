# ArtGalleryApp

## Overview
ArtGalleryApp is an iOS application that allows users to explore and manage art collections. Built using Swift and SwiftUI, the app leverages Core Data for local storage and integrates networking for fetching art-related data.

## Features
- **Browse Artworks**: View a curated collection of artworks.
- **User Profiles**: Manage user data and preferences.
- **Offline Support**: Save and access data using Core Data.
- **Networking**: Fetch and update content via APIs.

## Technologies Used
- **Swift** & **SwiftUI**
- **Core Data** for local storage
- **Networking** with API integration
- **Firebase (GoogleService-Info.plist)** for backend support
- **XCTest** for unit testing

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/ArtGalleryApp.git
   cd ArtGalleryApp
   ```
2. Open the Xcode project:
   ```sh
   open ArtGalleryApp.xcodeproj
   ```
3. Install dependencies if required.
4. Run the project on an iOS simulator or device.

 ## API Integration

1. The app fetches data from the Art Institute of Chicago API:
   ```sh
let baseURL = "https://api.artic.edu/api/v1/artworks?fields=id,title,artist_display,image_id,date_display,medium_display,dimensions,department_title"
```
2. The NetworkService fetches artwork data using Combine.
3. On a successful API response, artworks are displayed in the UI and saved in Core Data.

## Offline Mode
1. If the device is offline:
2. Cached artworks are retrieved using CoreDataManager.fetchCachedArtworks().
3. A message is displayed: "Offline mode: Showing cached data".

## License
This project is licensed under the MIT License - see the LICENSE file for details.

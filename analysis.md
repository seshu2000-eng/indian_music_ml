# Spotify Data Analysis Project

## Overview
This project analyzes music data from Spotify using the Spotipy API to extract insights about artists, albums, tracks, and playlist characteristics. The analysis focuses on Tamil/Kollywood music with some international tracks included.

## Data Collection

### API Setup
- Used Spotify's Web API with Client Credentials flow
- Client ID: `c855ed5e010e458b98d775a98e5800a5`
- Client Secret: `65268ef9226349fbb7f33043e61d3f60`

### Data Sources
1. **Artist Analysis**: G.V. Prakash and Yuvan Shankar Raja artist profiles
2. **Album Discovery**: Extracted all albums by Yuvan Shankar Raja
3. **Top Tracks**: Retrieved Yuvan's top 10 tracks in India
4. **Playlist Analysis**: Analyzed "Kollyywood Songs" playlist (100 tracks)

## Key Findings

### Artist Analysis
**G.V. Prakash**:
- Followers: 16,038,878
- Genres: Tamil pop, Kollywood, Tamil dance, Tamil hip hop, Tollywood

**Yuvan Shankar Raja**:
- Extensive discography with over 70 albums
- Top tracks include "Thuli Thuli", "Enkeyoo Partha", "Venmegam"

### Playlist Analysis
The analyzed playlist contains 100 tracks with varying popularity:

#### High Popularity Tracks (≥60)
- **Most Popular**: "Die With A Smile" by Lady Gaga (92)
- **Top Tamil Tracks**: Various songs by G.V. Prakash, Harris Jayaraj, and Yuvan Shankar Raja
- **International Hits**: Blinding Lights (The Weeknd), Closer (The Chainsmokers), STAY (The Kid LAROI)

#### Low Popularity Tracks (<60)
- Several tracks with 0 popularity, mostly older Tamil songs
- Includes classics by A.R. Rahman and Yuvan Shankar Raja

### Visualizations Created

1. **Plotly Plot**: Length vs Popularity by Artist
   - Shows no strong correlation between song length and popularity
   - Most songs cluster between 200,000-400,000 ms (3-6 minutes)
   - Popularity scores range widely across all durations

2. **Pie Chart**: Artist Distribution for High-Popularity Songs
   - Diverse artist representation in popular tracks
   - Mix of Tamil music composers and international artists

## Technical Implementation

### Data Processing
- Extracted track metadata: name, album, artist, release date, length, popularity
- Implemented pagination for large datasets (artist albums)
- Added rate limiting (0.3s delay between API calls)

### Data Storage
- Exported playlist data to CSV format for further analysis
- Structured data with clear column naming conventions

## Insights and Observations

1. **Popularity Distribution**: The playlist shows a bimodal distribution with very popular international hits and less popular regional content

2. **Artist Dominance**: Yuvan Shankar Raja has the most tracks in the playlist, reflecting his significant contribution to Tamil cinema music

3. **Temporal Trends**: Newer releases generally have higher popularity scores

4. **Genre Mix**: The playlist blends traditional Tamil film music with contemporary international pop

## Potential Applications

1. **Music Recommendation**: Understanding popularity patterns can inform recommendation algorithms
2. **Artist Analytics**: Track performance metrics for artists and composers
3. **Playlist Curation**: Data-driven insights for creating balanced playlists
4. **Market Analysis**: Understanding regional music preferences and international crossover appeal

## Limitations

1. **API Rate Limits**: Required careful pacing of requests
2. **Data Completeness**: Some audio features were not extracted in this analysis
3. **Sample Size**: Limited to 100 tracks from one playlist
4. **Regional Bias**: Focused primarily on Tamil music market

## Future Enhancements

1. Extract audio features (danceability, energy, acousticness, etc.)
2. Analyze temporal trends in music characteristics
3. Compare multiple playlists/genres
4. Implement predictive modeling for track popularity
5. Add sentiment analysis of lyrics (if available)

This analysis demonstrates the power of Spotify's API for music analytics and provides valuable insights into the characteristics of popular music in the Tamil market and beyond.
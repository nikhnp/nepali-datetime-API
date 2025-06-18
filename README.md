## Nepali Datetime Public API

Fork of [nepali-datetime-API](https://github.com/amitgaru2/nepali-datetime-API). Changed links to a working instance hosted with Koyeb.

### Basic Usage

1. To get today's Bikram Sambat Date

   ```sh
   curl -X GET https://date.nikhilnepal.com.np/date
   # returns { "data": "2077-06-26" }
   ```

   Response format can be changed by

   ```sh
   curl -X GET "https://date.nikhilnepal.com.np/date?format=%d-%B-%y"
   # returns { "data": "26-Aswin-77" }
   ```

   **More about the formatting in the table described [here](https://amitgaru2.github.io/nepali-datetime/html/index.html#strftime-and-strptime-behavior).**

1. Similarly, to get today's Bikram Sambat Date & current Nepal Time

   ```sh
   curl -X GET https://date.nikhilnepal.com.np/datetime
   # returns { "data": "2077-06-26 01:04:46.769648" }
   ```

1. Convert Bikram Sambat (BS) date to AD date

   ```sh
   curl -X GET 'https://date.nikhilnepal.com.np/date/convert/bs-ad?bs_date=2080-10-29&format=%Y-%m-%d'
   # returns { "data": "2024-02-12" }
   ```

1. Convert AD date to Bikram Sambat (BS) date

   ```sh
   curl -X GET 'https://date.nikhilnepal.com.np/date/convert/ad-bs?ad_date=2024-02-12&format=%Y-%m-%d'
   # returns { "data": "2080-10-29" }
   ```

`Formatting in 2., 3., 4. can be applied with the same approach as described in 1.`

## Use cases

1. Web pages and applications
1. Mobile applications
1. Desktop applications
1. Terminals / Consoles (zsh, tmux)

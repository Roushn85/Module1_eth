# MovieContract

## Description
MovieContract is a Solidity smart contract that provides functions for managing movie-related validations and recommendations. It includes features to validate viewer age, ticket prices, seat availability, and provides movie recommendations based on ratings and release year.

## Functions

### 1. validateAgeForMovie(uint age)

Ensures that viewers are at least 13 years old to watch the movie.

### 2. validateTicketPrice(uint ticketPrice)

Asserts that the ticket price is greater than 0 and does not exceed 100 units.

### 3. checkSeatAvailability(uint availableSeats, uint requestedSeats)

Reverts if there are not enough seats available for the requested group.

### 4. recommendMovie(bool isHighlyRated, uint releaseYear)

Recommends watching a newer or highly-rated movie based on certain conditions.

## Usage

1. Deploy the smart contract to the Ethereum blockchain.
2. Interact with the contract by calling its functions using a compatible Ethereum wallet or development environment.

## Example

```solidity
// Deploy the contract
MovieContract movieContract = new MovieContract();

// Validate viewer age
movieContract.validateAgeForMovie(15);

// Validate ticket price
movieContract.validateTicketPrice(75);

// Check seat availability
movieContract.checkSeatAvailability(100, 120);

// Recommend a movie
movieContract.recommendMovie(true, 2020);

# DECENTRALIZED-LOTTERY
# Decentralized Lottery Smart Contract

## Overview
This smart contract implements a decentralized lottery system built on Ethereum using Solidity. It allows participants to enter the lottery by sending Ether to the contract, and after a specified duration, the contract randomly selects a winner. The contract uses blockchain technology to ensure fairness, transparency, and security. 

This system is designed to be managed by a single "manager" address (usually the contract creator), who can declare the winner after the lottery ends. The contract is secure and protected against reentrancy attacks with OpenZeppelin's `ReentrancyGuard`.

## Objective
The goal of this project is to provide a fair and transparent decentralized lottery system that operates without intermediaries. Players participate by sending Ether to the contract, and at the end of the lottery period, a random winner is selected and awarded the accumulated prize pool.

## Features
- **Participation**: Users can enter the lottery by sending Ether to the contract, with a minimum contribution specified by the contract owner.
- **Manager-Only Actions**: The contract owner (manager) has the ability to declare the winner after the lottery period ends.
- **Lottery Duration**: The contract specifies the duration of each lottery round (in minutes).
- **Winner Selection**: The winner is selected randomly using a simplified randomness mechanism based on `block.prevrandao`. (Note: This is not secure for production and can be replaced with Chainlink VRF for better randomness.)
- **Transparency**: All transactions and events (participation, winner declaration, etc.) are logged on the blockchain, making the system fully transparent.
- **Security**: The contract is protected against reentrancy attacks using OpenZeppelin's `ReentrancyGuard`.
- **Fallback for No Participants**: If there are fewer than 3 participants, the lottery does not proceed, ensuring a reasonable chance of winning.

## Technologies Used
- **Solidity**: Smart contract language for building Ethereum-based decentralized applications.
- **Ethereum**: Blockchain platform for deploying and interacting with the contract.
- **OpenZeppelin Contracts**: A library of secure and community-vetted smart contract components, specifically `ReentrancyGuard` for attack prevention.
- **Smart Contracts**: The core of the lottery logic, utilizing Solidity to define the participation mechanism, random number generation, and prize distribution.



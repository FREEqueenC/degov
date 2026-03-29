# DeGov Launcher

[DeGov.AI](https://github.com/ringecosystem/degov) is an open-source, on-chain governance platform built for DAOs in the Ethereum ecosystem. This repository provides a Docker Compose configuration for launching a DeGov instance—the simplest way to set up your own governance platform.

## EIP Reference

This repository includes EIP documentation relevant to delegated staking governance:

- **[EIP-8205: Withdrawal credentials preregistration](EIPS/eip-8205.md)** — Introduces a mechanism for validator key holders to commit to specific withdrawal credentials before any deposit is made, addressing a known deposit front-running vulnerability in delegated staking protocols. Relevant to any DAO governing staking infrastructure. See also: [ethereum/EIPs#11450](https://github.com/ethereum/EIPs/pull/11450).

## Getting Started

1. Customize your DAO configuration

    The [degov.yml](degov.yml) file is critical for configuring your DeGov. It defines your DAO's name, logo, governance parameters, and contract addresses for interaction. Follow the commented instructions to customize your governance parameters.

2. Prepare your environment variables

    Copy [.env.sample](.env.sample) to `.env` and follow the instructions to update your environment variables.

3. Run `docker compose up -d` to start the DeGov instance and verify all services are running.
4. Visit http://localhost:3002 to access your DAO's DeGov interface. Note that it may take some time to sync blockchain data.

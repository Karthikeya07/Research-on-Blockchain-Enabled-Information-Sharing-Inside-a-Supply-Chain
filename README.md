# Blockchain-Enabled Information Sharing in Supply Chain

A research project and implementation demonstrating blockchain technology for secure and transparent information sharing within a supply chain ecosystem.

## Overview

This project implements a blockchain-based supply chain management system using Python and Django. It demonstrates how blockchain technology can enhance transparency, traceability, and security in supply chain operations by creating an immutable ledger of transactions.

## Features

- **Blockchain Implementation**: Custom blockchain with Proof-of-Work consensus mechanism
- **Supply Chain Tracking**: Track products through various stages of the supply chain
- **Transaction Management**: Secure recording of orders and transfers
- **Order Management**: Browse products and place orders
- **Immutable Records**: All transactions are permanently recorded on the blockchain
- **Data Integrity**: Cryptographic hashing ensures data cannot be tampered with

## Project Structure

```
├── supply-chain-app/        # Main Django application
│   ├── SupplyChain/        # Django project configuration
│   ├── SupplyChainApp/     # Main application module
│   ├── Blockchain.py       # Blockchain implementation
│   ├── Block.py            # Block class definition
│   └── manage.py           # Django management script
├── docs/                    # Documentation and research materials
│   ├── Final Report.pdf    # Complete research report
│   ├── IJRASET49373-Publication.pdf  # Published paper
│   ├── PPT.key            # Presentation slides
│   ├── Poster.key         # Research poster
│   └── images/            # Project screenshots and diagrams
├── requirements.txt        # Python dependencies
└── README.md              # This file
```

## Technology Stack

- **Backend**: Django 2.1.7
- **Language**: Python 3.x
- **Database**: MySQL (via pymysql)
- **Cryptography**: SHA-256 hashing, AES encryption
- **Blockchain**: Custom implementation with PoW

## Installation

### Prerequisites

- Python 3.7 or higher
- MySQL Server
- pip (Python package manager)

### Setup Instructions

1. Clone the repository:
```bash
git clone <repository-url>
cd Research-on-Blockchain-Enabled-Information-Sharing-Inside-a-Supply-Chain
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Configure database settings:
   - Update database credentials in [supply-chain-app/SupplyChain/settings.py](supply-chain-app/SupplyChain/settings.py)
   - Create a MySQL database for the application

5. Run migrations:
```bash
cd supply-chain-app
python manage.py migrate
```

6. Start the development server:
```bash
python manage.py runserver
```

7. Access the application at `http://localhost:8000`

## Usage

### For Customers
- Browse available products
- Place orders through the web interface
- Track order status

### For Supply Chain Participants
- View all orders in the blockchain
- Verify transaction integrity
- Monitor supply chain activities

### Blockchain Operations

The application automatically:
- Creates a genesis block on first run
- Mines new blocks when transactions are added
- Validates block integrity using Proof-of-Work
- Persists blockchain data to `blockchain_contract.txt`

## Blockchain Architecture

### Block Structure
Each block contains:
- **Index**: Block number in the chain
- **Transactions**: List of transactions in the block
- **Timestamp**: Block creation time
- **Previous Hash**: Hash of the previous block
- **Nonce**: Proof-of-Work nonce value
- **Hash**: Current block hash

### Consensus Mechanism
- Proof-of-Work with difficulty level 2
- Blocks must have hash starting with "00"
- Prevents tampering through computational requirements

## Research Documentation

This project is based on systematic literature review research. Full documentation available in the [docs](docs/) folder:

- **Final Report**: Comprehensive research findings
- **Published Paper**: IJRASET publication
- **Presentation**: Project presentation slides
- **Poster**: Research poster

## Security Considerations

- **Note**: This implementation includes a hardcoded Django SECRET_KEY in [settings.py](supply-chain-app/SupplyChain/settings.py:23). For production use, move this to environment variables.
- **Database**: Configure proper database authentication before deployment
- **DEBUG Mode**: Disable DEBUG mode in production environments

## Contributing

This is a research project. If you'd like to contribute or have suggestions, please open an issue or submit a pull request.

## License

See LICENSE file for details.

## Research Citation

If you use this work in your research, please cite the published paper available in the [docs](docs/) folder.

## Contact

For questions or collaboration opportunities, please open an issue in this repository.

## Acknowledgments

This project was developed as part of research on blockchain-enabled information sharing within supply chains.

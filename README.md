[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<br />
<div align="center">
  <a href="https://github.com/celikfatih/kafka-cluster-with-analytical-tools/">
    <img src="images/main-logo.svg" alt="Logo" width="100" height="100">
  </a>

<h3 align="center">Kafka Cluster with Analytical Tools</h3>

  <p align="center">
     It is a Docker environment that includes a Kafka cluster and various analytical tools.
    <br />
    <a href="https://github.com/celikfatih/kafka-cluster-with-analytical-tools/">
    <br />
    <a href="https://github.com/celikfatih/kafka-cluster-with-analytical-tools/issues">Report Bug</a>
    ·
    <a href="https://github.com/celikfatih/kafka-cluster-with-analytical-tools/issues">Request Feature</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

This project is designed to create a `Kafka` cluster in Docker. Afterwards, `OpenSearch` and `PostgreSQL` were added to the project for use in various analytical studies. 

New technologies will continue to be added to the project for use in analytical studies. You can access these details from the [Roadmap](#roadmap) section.

## Getting Started

To run locally, follow the steps below.

### Prerequisites

To run locally, you must first have `docker` and `docker-compose`.

- [Here's](https://docs.docker.com/desktop/) how to download Docker to your local environment.
- [Here's](https://docs.docker.com/compose/install/) how to download Docker Compose to your local environment.

### Installation

1. First of all, it should be checked that `docker` and `docker-compose` are running.

2. Clone the repo:
   ```sh
   git clone https://github.com/celikfatih/kafka-cluster-with-analytical-tools.git
   ```
3. Specify the values of the parameters in the `.env` file.

   - `POSTGRES_PASSWORD`: User password for PostgreSQL.
   - `POSTGRES_USER`: Username for PostgreSQL.
   - `POSTGRES_DB`: Default database name for PostgreSQL.
   - `PGADMIN_EMAIL`: PgAdmin default email address.
   - `PGADMIN_PASSWORD`: Password for PgAdmin user login.
   - `PGADMIN_USER`: Username for PgAdmin login.

4. Inside the project, to start kafka-cluster (The `-d` parameter optional and allows it to run in the background):
   ```sh
   docker-compose up -d
   ```
5. If no errors have occurred, your Kafka cluster is ready in ports `:9092, :9093, :9094`.
6. In the browser for PgAdmin, you just need to go to `127.0.0.1:8080`.
7. To access OpenSearch Dashboard, you just need to go to `127.0.0.1:5601` in the browser.

## Usage

To use Kafka, you can give your applications any address between `127.0.0.1:9092-9094`. Since there is a kafka cluster, it will be enough for you to specify the address of any broker.

You can use `127.0.0.1:5432` to use Postgres as a database in your applications. It will also be enough to go to `127.0.0.1:8080` in your browser to access PGAdmin.

Finally, to use OpenSearch, you can use `127.0.0.1:9200` as an address in your applications. To analyze indexes, you can reach OpenSearch Dashboard at `127.0.0.1:5601`.

## Roadmap

- [x] Add Kafka
- [x] Add Postgres
- [x] Add PGAdmin
- [x] Add OpenSearch
- [x] Add OpenSearchDashboards
- [ ] Different components will be added that can work with Kafka.
  - [ ] Spark
  - [ ] Flink etc.

See the [open issues](https://github.com/celikfatih/kafka-cluster-with-analytical-tools/issues) for a full list of proposed features (and known issues).

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the GNU General Public License v3.0. See `LICENSE` for more information.

## Contact

Fatih Celik - [@celikfatii](https://twitter.com/celikfatii) - celikfatih@protonmail.com

Project Link: [https://github.com/celikfatih/kafka-cluster-with-analytical-tools/](https://github.com/celikfatih/kafka-cluster-with-analytical-tools/)

## Acknowledgments

- [Img Shields](https://shields.io)
- [Best-README-Template](https://github.com/othneildrew/Best-README-Template)
- [Kafka]()

[contributors-shield]: https://img.shields.io/github/contributors/celikfatih/kafka-cluster-with-analytical-tools.svg?style=for-the-badge
[contributors-url]: https://github.com/celikfatih/kafka-cluster-with-analytical-tools/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/celikfatih/kafka-cluster-with-analytical-tools.svg?style=for-the-badge
[forks-url]: https://github.com/celikfatih/kafka-cluster-with-analytical-tools/network/members
[stars-shield]: https://img.shields.io/github/stars/celikfatih/kafka-cluster-with-analytical-tools.svg?style=for-the-badge
[stars-url]: https://github.com/celikfatih/kafka-cluster-with-analytical-tools/stargazers
[issues-shield]: https://img.shields.io/github/issues/celikfatih/kafka-cluster-with-analytical-tools.svg?style=for-the-badge
[issues-url]: https://github.com/celikfatih/kafka-cluster-with-analytical-tools/issues
[license-shield]: https://img.shields.io/github/license/celikfatih/kafka-cluster-with-analytical-tools.svg?style=for-the-badge
[license-url]: https://github.com/celikfatih/kafka-cluster-with-analytical-tools/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/cefatihcelik
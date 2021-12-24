# amp-wp-dev
Development environment for amp-wp plugin

## Get Started

1. Clone the Git repo with submodules
```
git clone https://github.com/ediamin/amp-wp-dev.git --recursive
```

2. Build AMP WP plugin and WordPress Develop
```
npm install
```

3. Start wp-env
```
npm start
```

Dev Site: http://localhost:1234
username: admin
password: password

## PHP Unit Testing
Run all tests
```
npm run phpunit
```

Run specific test file
```
npm run phpunit --args=./tests/php/test-amp.php
```

Run specific test method
```
npm run phpunit --args='./tests/php/test-amp.php --filter=test_amp_is_canonical'
```

## Notes
1. `npm start` will spin up docker with [xdebug](https://github.com/WordPress/gutenberg/blob/trunk/packages/env/README.md#xdebug-ide-support). It is available in both wordpress and test-wordpress containers. VSCode configuration is already in this repo.
2. Not sure why some tests fail in `tests-cli` container.
3. `phpunit` in `phpunit` container won't work because we need lower version of phpunit to run the tests.

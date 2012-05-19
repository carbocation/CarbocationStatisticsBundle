CarbocationStatisticsBundle
===========================

This is a pure PHP library that implements multivariate linear regression using 
linear algebra.  The Moore-Penrose pseudoinverse is used in the computation of the 
coefficient matrix. The original regression and matrix libraries were 
written by Shankar Manamalkav, and the original files can be found 
[on his blog](http://mnshankar.wordpress.com/2011/05/01/regression-analysis-with-php/). 
It has been adapted as a Symfony2 bundle by James Pirruccello.

This bundle is covered by the MIT license. For details, 
[see the license](https://github.com/carbocation/CarbocationStatisticsBundle/blob/master/Resources/meta/LICENSE).

Symfony2 Installation
---------------------
This bundle can be used as a standalone package for PHP 5.3+. It can also be used 
as a Symfony2 bundle. 
To do so, follow these instructions (for the 2.0.x branch):

1.  Add this bundle to your `deps` file:

        [CarbocationRegressionBundle]
            git=git://github.com/carbocation/CarbocationStatisticsBundle.git
            target=/bundles/Carbocation/StatisticsBundle

    Then run `bin/vendors install`.

2.  Register the `Carbocation` namespace in the `app/autoload.php` file:

        $loader->registerNamespaces(array(
            // ...
            'Carbocation'      => __DIR__.'/../vendor/bundles',
        ));

3.  Register the bundle in the `app/AppKernel.php` file:

        public function registerBundles()
        {
            $bundles = array(
                // ...
                new Carbocation\StatisticsBundle\CarbocationStatisticsBundle(),
            );
        }

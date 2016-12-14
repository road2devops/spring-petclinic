node('node') {


    currentBuild.result = "SUCCESS"

    try {

       stage 'Checkout'

            checkout scm
              mail body: 'project build successful',
                        from: 'haritha_burle@contractor.amat.com',
                        replyTo: 'xxxx@yyyy.com',
                        subject: 'project build successful',
                        to: 'haritha_burle@contractor.amat.com'

        }


    catch (err) {

        currentBuild.result = "FAILURE"

            mail body: "project build error is here: ${env.BUILD_URL}" ,
            from: 'xxxx@yyyy.com',
            replyTo: 'yyyy@yyyy.com',
            subject: 'project build failed',
            to: 'zzzz@yyyyy.com'

        throw err
    }

}

// pipeline {
//     agent any 
//     stages {
//         stage('Build') { 
//             steps {
//                 bat 'python -m py_compile sources/add2vals.py sources/calc.py' 
//                 stash(name: 'compiled-results', includes: 'sources/*.py*') 
//             }
//         }
//     }
// }


// This is testing the pipeline with a different approach to the build stage. The previous approach was using a Linux shell command, while this one is using Windows batch commands. The 'where python' command checks if Python is installed and available in the system's PATH, and 'python --version' retrieves the installed Python version.
// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             steps {
//                 bat 'where python'
//                 bat 'python --version'
//             }
//         }
//     }
// }



// stage 2 trial for jenking file
// pipeline {
//     agent any

//     stages {

//         stage('Build') {
//             steps {
//                 bat '"C:\\Users\\srbht\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" -m py_compile sources\\add2vals.py sources\\calc.py'

//                 stash(
//                     name: 'compiled-results',
//                     includes: 'sources/*.py*'
//                 )
//             }
//         }
//     }
// }

/// this is chekin where is python and python version
pipeline {
    agent any

    stages {

        stage('Build') {
            steps {

                bat '"C:\\Users\\srbht\\AppData\\Roaming\\uv\\python\\cpython-3.11.15-windows-x86_64-none\\python.exe" --version'
                //bat '"C:\\Users\\srbht\\AppData\\Roaming\\uv\\python\\cpython-3.11.15-windows-x86_64-none\\python.exe" -m py_compile sources\\add2vals.py sources\\calc.py'
                bat '"C:\\Users\\srbht\\AppData\\Roaming\\uv\\python\\cpython-3.11.15-windows-x86_64-none\\python.exe" -m py_compile sources\\*.py'
                stash(
                    name: 'compiled-results',
                    includes: 'sources/*.py*'
                )
            }
        }
    }
}
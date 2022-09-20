1. Create structure package
```
    /packaging_tutorial
        /example_pkg
            __init__.py
            app.py
        setup.py
        LICENSE
        README.md
```
2. In file __init__.py
    ```
        from app import *
    ```
3. In file app.py
    ```

    def sum(a, b):
        return a + b

    def hello():
        print("Hi everyone of group 19NH11")

    def member_team():
        print("Include 4 members: ")
        print("\tPhan Van Binh")
        print("\tLe Thanh Quy")
        print("\tNguyen Thanh Co")
        print("\tTran Nguyen Anh Trinh")
        print("\tLe Van Huy")

    ```
4. In file setup.py
    ```
    import setuptools

    setuptools.setup(
        name="pythonbchqt",
        version="1.0.1",
        author="BinhPhanVan",
        author_email="phanvanbinh192837@gmail.com",
        description="Sort description",
        long_description="Full description",
        long_description_content_type="text/markdown",
        url="https://github.com/pypa/sampleproject",
        packages=setuptools.find_packages(),
        classifiers=[
            "Programming Language :: Python :: 2",
            "License :: OSI Approved :: MIT License",
            "Operating System :: OS Independent",
        ],
    )

    ```
5. In file README.md
    Insert content for funtion, which you write in file app.py
6. In file LICENSE
    ```
    MIT License

    Copyright (c) 2019 minhhahao

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

    ```
7. Install library
    ```
    pip install -U setuptools wheel
    ```
8. Package file
    ```
    python setup.py sdist bdist_wheel
    ```
9. Upload distribution archives
    ```
    pip install -U twine

    python -m twine upload --repository-url http://localhost:8081/repository/<repo-name>/ dist/*
    ```
10. In windows 
    create file pip.ini in path :   C:\ProgramData\pip
    with content
    ```
    [global]
    index = http://localhost:8081/repository/<repo-name>/pypi
    index-url = http://localhost:8081/repository/<repo-name>/simple
    ```
11. Share localhost with ngrok
12. Documentation

    (viblo)[https://viblo.asia/p/huong-dan-tao-package-python-RnB5pBvDZPG?fbclid=IwAR2abgXrSTj1U_pSQm30xfYtLgZe5duMIHhYf11C18OEdC7-BaRpQxt5wpY#_upload-distribution-archives-4]
    (sonatype)[https://help.sonatype.com/repomanager3/nexus-repository-administration/formats/pypi-repositories?fbclid=IwAR0i3f2nT37aD3KL6NYWKkmD6rWw_GPlfy885mib2__6yWTpoQL9C3whe08]
    (github)[https://github.com/renardeinside/nexus_pypi_repo_example?fbclid=IwAR2qi_2Ox7432cWPrxpByPr2msGLmOVzVDFngV2ZKDeK9R3d9b5vz4ljyuI]
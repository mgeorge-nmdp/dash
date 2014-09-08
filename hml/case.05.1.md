### Example 5.1

Lab 999 typed a sample for center 123 for the ABDR project.\
 The typing was performed on Jan 23, 2004.\
 The results are:\

        NMDP ID: 444-333-2   A*0102, A*0103
                             A*0103, A*0106
          

------------------------------------------------------------------------

Using allele codes this result would be reported as `A*01BC, A*01CF`,
using the following xml:

      <?xml version="1.0" encoding="UTF-8"?>
      <!DOCTYPE hml PUBLIC "-//NMDP//DTD HML 0.3//EN" "http://www.nmdp.org/DTD/hml-0.3.dtd">
      <hml version="0.3">
        <project name="ABDR">
          <reporting-center code="999"/>
          <sample id="444-333-2" center-code="123">
            <typing>
              <interpretation date="20040123">
                <haploid locus="A" method="DNA" type="01BC"/>
                <haploid locus="A" method="DNA" type="01CF"/>
              </interpretation>
            </typing>
          </sample>
        </project>
      </hml>

------------------------------------------------------------------------

Starting in HML 0.3, this result can be reported as a genotype list,
using the following xml:

      <?xml version="1.0" encoding="UTF-8"?>
      <!DOCTYPE hml PUBLIC "-//NMDP//DTD HML 0.3//EN" "http://www.nmdp.org/DTD/hml-0.3.dtd">
      <hml version="0.3">
        <project name="ABDR">
          <reporting-center code="999"/>
          <sample id="444-333-2" center-code="123">
            <typing>
              <interpretation date="2004-01-23">
                <genotype-list db="HLADB" version="2.4.0">
                  <diploid-combination>
                    <locus-block>
                      <allele-list>
                        <allele>A*0102</allele>
                      </allele-list>
                    </locus-block>
                    <locus-block>
                      <allele-list>
                        <allele>A*0103</allele>
                      </allele-list>
                    </locus-block>
                  </diploid-combination>
                  <diploid-combination>
                    <locus-block>
                      <allele-list>
                        <allele>A*0103</allele>
                      </allele-list>
                    </locus-block>
                    <locus-block>
                      <allele-list>
                        <allele>A*0106</allele>
                      </allele-list>
                    </locus-block>
                  </diploid-combination>
                </genotype-list>
              </interpretation>
            </typing>
          </sample>
        </project>
      </hml>
        

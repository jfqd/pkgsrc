# $NetBSD: Makefile,v 1.17 2017/11/13 14:24:51 wiz Exp $

DISTNAME=	XML-LibXML-Simple-0.98
PKGNAME=	p5-${DISTNAME}
CATEGORIES=	textproc perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=XML/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/XML-LibXML-Simple/
COMMENT=	XML::LibXML clone of XML::Simple
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-File-Slurp-Tiny-[0-9]*:../../devel/p5-File-Slurp-Tiny
DEPENDS+=	p5-XML-LibXML>=1.64:../../textproc/p5-XML-LibXML

# TEST_DEPENDS
BUILD_DEPENDS+=	p5-Test-Pod>=1.00:../../devel/p5-Test-Pod

EXTRACT_USING=	bsdtar

PERL5_PACKLIST=		auto/XML/LibXML/Simple/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
